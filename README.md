# Introduction to git and github

This repo is a basic introduction to version control using git and github. 

[Here is the presentation link](https://docs.google.com/presentation/d/1XIyhUT9wJpH0moAUFvryOWQfO-txDT6yg7_mjEGFxPs/edit?usp=sharing)

### In this workshop, we cover:
- What are version control systems
- Creating a brand new git repository with versioned files
- Pushing to github
- Branches: checkout/switch, merge, push

### Important Concepts
Hidden files
Files that start with a . are hidden. There are two to be aware of for this workshop
```sh
.git

.gitignore
```

To view hidden files in a directory, use `ls -a`

Git stores a snapshot of your project

Your project in git is stored in a repository

### Working on a project with git follows this pattern:

*Edit / add / commit /push*

```sh
# Edit your files with your new content using your favorite text editor.

git add <filename> # add a change to the staging area.

#or

git add . # add all new files to the staging area.

git commit -m "commit message" # take a snapshot of the project

# If you're only modifying existing files, you can perform the above two steps in a single step
git commit -am "commit message"

# Push to github
git push

#or

git push -u origin <branch_name>
```

#### Git terminolgy
`clone` - copy a respository to your computer so you can work on it

`fork` - copy a respotiory for independent development

`commit` - make a snapshot of the repository

`branch` - branch off from the main developement to work on something

#### Git - where am I?
`git log` - see what commit you're on

`git remote -v` - see what remote repository you are tracking

`git branch` - find out what branch you are on

#### Viewing your changes
`git status` - see any edits you made

`git diff` - show difference between your files and the commited files

`git diff` --cached same as diff, but for files you have already added

#### Reverting changes
`git log --oneline` - a condense way to view the log

`git revert` - undo history but keep a record

`git reset` - undo history like it never happened **Beware**

#### Working with remotes
`git pull` - get changes from the remote repository

`git push origin main` - send your changes up to the remote repository

#### Storing local changes while you pull from a remote repository

Some times the changes you pull from a remote repository will conflict with your local changes. You can stash your local changes, pull the new changes from the remote repository, then pop your changes back.

`git stash`

`git stash pop`

