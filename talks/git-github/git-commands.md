# Introduction  Git and Github

>> Create by linux trovals
##Objective

* leraning more about git


## Getting started with git

#### Setup
* git config --global user.name "user name here"
* git config --global user.email "email here"
* git help

#### Create a projects
git init
git clone


#### Some commands basic in GIT
```
git status
git diff
git add <name-file>
git add .
git add --all
git add *.txt
git add docs/*.txt
git add docs/
git add "*.txt"
git commit
git reset
git rm
git mv
git log
HEAD is refers to our last commint in timeline.
testing command git checkout -- "file-name" , blow away all changes since last commit
git commit -a -m "Modify readme"
-a (Add changes from all tracked files)
-m (commit message)
git reset --soft HEAD^ , reset into staging   move to commit before "HEAD"
Maybe we forgot to add a file in lasts commit ?? :(
git add todo.txt
git commit --amend -m "Modify readme & add todo.txt"
git reset --hard HEAD^ undo last commit and all changes
git reset --hard HEAD^^ undo last 2 commit and all changes
git remote add origin <link-here>
git push -u origin master
git pull origin master or git pull
Working with remotes
git remote add <name> <address>
git remote rm <name>
git push -u <name> <branch>
```

## Cloning & Branching
```
git branch <name-branch>
git checkout <name-branch>, switch to branch
in branch master you type
git marge cat
remove branch
git branch -d cat
git checkout -b admin, create new branch and switch
Now we will create a new file and then add and commit.
git add <new-file>
git commit -m "Add new file"
now we'll get back to that admin branch later, and fix bug.
git checkout master
git pull
git add <file-fix-fug>
git commit -m "Fix store bug"
git add <new-bug-fix>
git  commig -m "Fix bug in porduc"
git push origin master
now we'll back to our branch.
git checkout admin
git checkout master
git merge admin
git will create orde commit (recursive commit)
```
## Collaboration basics
```
Cannot write over "User's" commit, because local repository and github repository not is the same
(not is equal, not is the same code )
git fetch, Fetch (or Sync) our local repository with the remote one, going to copy down (github repository)
into our.. then we'll git merge origin/master
git push
git push origin/master
Merge conflicts in same file, user1 create local repository and user2 committed and pushed to Github.
git pull (conflict)
then we edit file manually and delete all the extra text and make it, and then.
git commit -a
git merge (name)
git push
```
## Branching
```
When you neet other people to work on your branch.
Any branch that will last more than a day
git checkout -b shopping_cart
git push origin shopping_cart
git add card.rb
git commit -a -m "Add new card.rb"
git branch
git branch -r
git checkout shooping_cart
git remote show origin
```
## Tagging
```
A tag is a reference to a commit (used mostly for release versioning)
git tag , list all tag
git checkout <tag-name>, check out code at commit
git tag -a v0.0.3 -m "version 0.0.3"
git push --tags
```
## Rebase Belong to Us
```
Merge commits are bad.
git rebase.
1. Move all changes to master which are not in origin/master to a temporary area.
2. Run all origin/master commits.
3. Run all commits in the temporary area, one at a time.
git rebase --continue
git rebase --abort
git rebase --skip
```
## History and configuration
```
git log
git log --pretty=oneline
git log --pretty=oneline --graph
git log --pretty=oneline --graph --all
filters since
git log --since='Jan 2 2018'
filters until
git log --until='Jan 2 2018'
git log --since='Jan 1 2018' --until='Jan 8 2018'
git log --author='Matheus'
simple log
git shorlog
git shorlog -sn
git reflog
git reflog
git diff
git blame <file-name> --date short
output : commit hash, author, date, line # content
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
```
