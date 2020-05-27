# Git and GitHub Command-Line Tutorial

---

![alt text](https://imgs.xkcd.com/comics/git.png)

---

# Workflow Quick-Reference

The essential chunk of code - use this and you're 99% there.

```
git pull
<add code, etc.>
git add <filename> (use * to add all files)
git commit -m '<message here>'
git pull (avoid tangled commits)
git push
```

---
---

# 1) GitHub Setup

These steps are only required once.

1. [Go to GitHub](https://github.com/) and create an account with a valid email address.
2. [Download the proper version of git for your OS.](https://git-scm.com/)
3. Open up your terminal, check for git:
    * ```$ git --version```
4. Check your configurations:
    * ```$ git config --list```
5. If you don't see your name and email:
    * ```$ git config --global user.name "<your name on GitHub>"```
    * ```$ git config --global user.email "<your email on GitHub>"```
    
---
    
# 2) Repository Setup
    
These steps are required every time you want to collaborate on a new repository.
    
**Clone vs Fork:** Making a **clone** gives you a private copy of a repo; only you will see any changes made, so this will mainly be used for testing. A **fork** creates a local repo in your GitHub account; you can request to merge any changes with the master repo.
    
### Forking and Cloning Steps
    
1. Go to the repository you want to fork: [here](https://github.com/nkelley-uga/github_tutorial)
2. Click **Fork** in the upper right.
3. Go to your fork: ```https://github.com/<your-username>/github_tutorial```
4. Clone your fork:
    * click the green button that reads *Clone or download*
    * copy the url
    * open terminal
    * go to the directory you want to store in, ex: ```$cd Documents/```
    * make clone: ```$ git clone https://github.com/<your-username>/github_tutorial.git```
5. Change directory into your clone: ```$ cd github_tutorial```
6. Check references (where you can push and pull): ```$ git remote -v```
7. Give your local repo option to go upstream: ```$ git remote add upstream https://github.com/nkelley-uga/github_tutorial```
8. Check that "upstream" is available: ```$ git remote -v```
    
---    
    
# 3) Example Workflow
    
The steps for merging your work and work from your team, by example:
    
1. Sync up: ```$ git pull upstream master```
    * note: ```$ git pull``` will only pull from your fork
2. cd into submission folder: ```$ cd practice_submits```
3. make a small test file: ```$ echo "<your-text>" > <your-name>.txt```
4. check status: ```$ git status```
5. add your new work: ```$ git add <your-file>```
6. check status: ```$ git status```
7. stage your file: ```$ git commit -m "added new file"```
8. check status: ```$ git status```
9. send changes to your local repo: ```$ git push```
10. check status: ```$ git status```
11. sync repos: ```$ git pull upstream master```
12. Make a pull request:
    * go to your fork: https://github.com/<your-username>/github_tutorial.git
    * click: "New pull request"
    * click: "Create pull request"
    * fill: "Leave a comment"
    * click: "Create pull request"
    
---
---
    
# Local Storage Tip
    
In addition to your local clone, keep a separate folder (your "sandbox") where you can make any and all changes. When you're ready to submit any changes, copy them into your clone and submit a pull request.
    
---
    
# Some Useful Links
    
* [GitHub Desktop](https://desktop.github.com/)
* [GitHub Cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code)
* [Markdown Math Reference](https://www.calvin.edu/~rpruim/courses/s341/S17/from-class/MathinRmd.html)
* [Simple Git Guide](http://rogerdudler.github.io/git-guide/)
* [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)