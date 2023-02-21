# Git Simple Tutorial

## Description
---
Just a simple tutorial on how to use git and github/bitbucket

### Explanation
---
Git is for version control. So you can undo and redo your code easily, by going to specific "commits". We can think of commits as our saved checkpoints. Read the git documentation for more details.

Github and Bitbucket is just platforms to "store" your repository in the cloud / online. A repository (repo) is just a project that you have.

The repo is almost usually always on the cloud, so we can access it from any device. But when we are working on the repo in our local device, we will need to clone the repo into our local device. Any changes that we make will only be on the local repo, until we push it onto the cloud (github / bitbucket). Think of it as when you are working on a document on your laptop. When you save it, it will just save on your laptop. However, to work on the same document in another of our device, you will have to save this document onto OneDrive/iCloud or any cloud provider. Then on your other device, you will sync (try to bring the latest changes) onto that device.

### Git Workflow
---
There are many workflows out there, usually depends on how the team chooses to do it. No fixed way. But the following is my preferred way. (trunk workflow)
* we will have a main/master branch. this branch can be thought of as the source of truth and only work that is approved by everyone and is the ready version will be pushed onto this branch.
* for each developer, we will create our own sub branch (I use my own name for this branch), lets call it the namebranch. we can think of this sub branch as our individual "main" branch. anything that i push here will be "ready" on my side. anything on this branch will then be used to submit a pull request on the main/master branch above.
* any feature or smaller stuff that i want to work on will be subbranches of the namebranch, and when those features are done, i will merge it onto my namebranch.
* some good practices
  * commit often
  * git pull and merge conflict from main trunk often

### Additional notes for hackathon:
1. create the repo on github
2. optional step: fork the repo instead of directly working on it (usually only used in open source projects)
3. each developer will clone the repo onto their own local to work on it
4. create your name branch
5. you can choose to just commit everything on your name branch if you are lazy
6. commit often
7. switch to the master branch and pull (from online) once in awhile (to sync your local repo with any new changes from teammates)
8. when u are done working with some feature, push you namebranch onto the online repo
9. go to github and submit a pull request (to combine your changes into the master branch)
10. if your pull request is successful (approved by teammates), then the master branch will now have your feature. your teammates will have to pull from the cloud repo to get these changes on their local

### Git commands:
---
Commonly used:
``` zsh
git clone repo_url
git stash
git stash pop
git pull
git checkout -b branchname (create and go to that new branch)
git checkout branchname
git switch -c branchname (create and go to that new branch)
git switch branchname
git add -A
git commit -m "message"
git push
git status
git log
git checkout to the branch to merge into, then run "git merge branchname" where branchname is the branch to be merged into the branch you are on 
git branch --delete branchname
git branch -m newname (do this on the branch oldname you want to rename)
```

Less commonly used:
```zsh
git rm
git help <verb> (full blown manual page)
-h (for quick refresher) e.g: git add -h
q (to back)
command line: rm -rf to remove a file/folder
git show <part of hash>
git checkout <tagname> / <branch hash> (means go to that point of commit)
git tag (to list all tags)
git tag <name> (lightweight)
git tag -a <tagname> -m <tag message>
git show <tag name>
master/head~2 to go back 2 commits
```

