# git-tips

##### Set your git details
```
git config --global user.name "Stevie Wonder"
git config --global user.email "stevie@example.com"
```
##### Initialize a git repo
```
git init
```
##### Clone a remote repo
```
git clone <url>
```
##### Update your current branch with remote
```
git pull origin master
```
##### Change origin URL
```
git remote set-url origin <url>
```
##### Add remote URL
```
git remote add <remote-name> <url>
```
##### View remote URLs
```
git remote -v
```
##### Create a branch locally
```
git checkout -b <branch-name>
```
##### Delete a branch locally
```
git branch -d <branch-name>
```
##### Show current branch
```
git branch
```
##### Switch to different branch
```
git checkout <branch-name>
```
##### Create a branch remotely
```
git push -u origin <branch-name>
```
##### Delete a branch remotely
```
git push origin :<branch-name>
```
##### Create a git alias
```
git config --global alias.st status
git config --global alias.ci commit -m
git config --global alias.cob checkout -b
```
##### Show unstaged changes you made since last commit
```
git diff
```
##### Stash local changes
```
git stash
```
##### Remove a single stashed state from the stash list and apply on top of the current working tree state
```
git stash pop
```
##### List all stashes
```
git stash list
```
##### Remove all stashed states
```
git stash clear
```
##### Add all files, including subdirectories
```
git add .
```
##### Undo all local changes
```
git reset --hard
```
##### Add individual files
```
git add <file1> <file2>...
```
##### Remove individual files
```
git rm <file1> <file2>...
```
##### Commit changes to all tracked files
```
git commit -m "<message>"
```
##### Re-commit previous commit with different message
```
git commit --amend -m "<message>"
```
##### Undo last local commit
```
git reset --soft HEAD^
git reset HEAD .
```
##### Rebase to local master
```
git rebase master
```
##### Push local branch
```
git push origin <branch-name>
```
##### Squash multiple commits
```
git rebase -i master
```
##### Comapre commits on 2 different branches
```
git diff <branch-name1> <branch-name2>
```
##### Revert one commit and push it
```
git revert <HASH>
git push origin master
```
##### Show recent commits
```
git log
```
##### Show recent commits with full diffs
```
git log -p
```
##### Show commit history in one line
```
git log --pretty=oneline
```
##### Delete all local branches but master
```
git branch | 
grep -v "master" | 
xargs git branch -D
```
##### Show all branches merged into master
```
git branch --merged master
```
##### Show all branches merged to HEAD(tip of current branch)
```
git branch --merged
```
##### Show all branches that have not been merged to master
```
git branch --no-merged
```
##### Delete all merged branches into master
```
git branch -r --merged |
grep origin |
grep -v '>' |
grep -v master |
xargs -L1 |
awk '{split($0,a,"/"); print a[2]}' |
xargs git push origin --delete
```
##### Update a github forked repo
```
git remote add upstream <parent-repo-url>
git fetch upstream
git rebase upstream/master
git push -f origin master
```
#### Git submoulde update
```
git submodule update --init --recursive
```
#### Delete untracked files
```
git clean -f -d
```
#### Adding an existing project to github
```
git init
git add .
git commit -m "commit message"
git remote add origin <remote repository url>
git push -u origin master
```
#### Set origin head for remote repo
```
git remote set-head origin <branch>
```

