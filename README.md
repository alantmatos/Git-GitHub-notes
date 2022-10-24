##
# **Introduction**



Imagine there is a team of developers working on a popular web application with many features. The app may have a large, complex code base which means that, at any given time, there are likely to be multiple projects going on and multiple developers working on different parts of the software.

This type of scenario is quite common, and can easily lead to problems:

- Imagine someone is working on a new feature, or incorporating a new technique, or refactoring the code to make it more efficient and something they change breaks the app. How can they "back up" to the most recent working version of the code?
- There could be some part of the application that overlaps with the work being done by more than one developer. How can they ensure that no inconsistencies or conflicts work their way into the code?
- How can they maintain a record of the changes that are being made and why? Over time, memories about how things have been done can fade, or new people may join the team who don't have that background knowledge. This can lead to inconsistencies in the code or to wasted time revisiting issues that have been addressed in the past.
- What if you are asked to implement or test a new feature? Testing on the current working code does not seem to be the best approach.

Well .. Thanks to the **version control system (VCS)**. There is a *somewhat easy* work around this.

**Git** =  Git is a VCS ( version control system ). A free and open source version control system (a way of tracking code changes, reverse to previous versions..etc).

**GitHub** = A website that hosts your repositories online.

## **Setup**

- Git [How to Check and Update Your Git Version (howtogeek.com)](https://www.howtogeek.com/759319/how-to-check-and-update-your-git-version/)
- Terminal
- Github account
- Text editor







#








## **Intro to Version Control**



Hackers and painters

[Hackers and Painters (paulgraham.com)](http://www.paulgraham.com/hp.html)
##
## **Identify Benefits of Version Control Systems**

There are a number of benefits we get when we use a VCS such as Git to manage our work:

- Automatically create a backup of our project.
- Provide an easy way to undo mistakes and restore a previous version of the project.
- Document changes with a log that describes what's been changed and why.
- Easily view the differences between two versions of the project.
- Branch work off into multiple "sandboxes" (called **branches** in Git) that allow developers to experiment without impacting other branches.
- Collaborate with others without disturbing each other's or our own work.

And beyond these are even more advanced features that will help you optimize your workflow once you've learned the basics







## **Useful Git Vocabulary Terms:**
We're about to get busy learning Git, but we first need to establish some common vocabulary. Git, perhaps more than any other software, has some special words that you'll hear a lot. Don't worry you will learn them as you go.

- **repository** (or **repo**, for short): A directory of files that are **tracked** by Git.
- **track**: When a file is **tracked** by Git, it means that Git will notice any changes to that file. We call these changes **differences** or **diffs**. Git allows you to choose whether to **commit** a diff in order to keep it.
- **diff**: The **diff** of a *file* is all the changes that have been made to it since the last **commit**. The **diff** of a *repo* is all the diffs in all the *tracked* files in the repo that have not yet been committed (sometimes programmers call this the **diffset**).
- **commit**: Once we decide we want to save a diff, we **commit** the diff to the repo's history using the commit command. When we make a commit, we write a **log** message that describes what happened in the diff. The set of commits provides a history of all of the changes that have been made to a repo and when.
- **log**: The record of what happened in each commit.
- **local/remote**: When we start working with an existing Git repo, we **clone** it from a **remote** source (on GitHub) and copy it to our machine. We call the repo on our personal system the **local** repo.
- **branch/default branch**: A Git repo can support multiple **branches** that make it possible for multiple developers to be working on the code at the same time. When you initialize a new Git repo, a **default branch** is created where your work will be tracked. Historically, Git has used master as the default name of the default branch, but many organizations in the Git community, including GitHub, are moving away from using master and using main instead. You will still see master used in many repos, especially older ones.







#
## **.gitignore**

In an earlier lesson, we mentioned that sometimes we don't want Git to track changes for all of the files in our repository. Git allows us to tell it to ignore specific files or directories in our project by using a .gitignore file. In this lesson, we'll discuss the types of things that might go into a .gitignore file as well as how to create one.

` `There are three main reasons why we want Git to ignore files:

1. Private files
1. Irrelevant files
1. Files that are too large for GitHub

##
## **Top Git Commands:**

1. git config –global user.name “[name]” ->sets author name
   git config –global user.email “[email address]” ->sets author email id
1. git –version ->Check if Git is installed and which version it is currently running.
1. ` `rm -rf .git -> Delete the git tracker, r to delete the .git folder and all its contents and return the directory to a plain-old, unprotected directory.
1. rm -rf [repoName]-> Delete the repository with the given name.
1. git rm --cached [filename.ext] -> Tell Git to stop tracking a given file.
1. git rm [file] ->deletes the file from your working directory and stages the deletion.
1. git init [repository name] ->start new repository
1. git clone [url] ->obtain a repository from an existing URL.
1. git add [file] ->adds a file to the staging area.

git add . ->adds all the files in the current directory to the staging area.

1. git commit -m “[ Type in the commit message]” ->records or snapshots the file permanently in the version history.
   git commit -a ->commits any files you’ve changed since then.&commits any files you’ve added
1. git diff ->shows the file differences which are not yet staged.
   git diff –staged ->differences between the files in the staging area and the latest version present.
   git diff [first branch] [second branch] ->differences between the two branches mentioned.
1. git reset [file] ->unstages the file, but it preserves the file contents.
   git reset [commit] ->undoes all the commits after the specified commit and preserves the changes locally.
   git reset –hard [commit] ->discards all history and goes back to the specified commit.
1. git status ->command lists all the files that have to be committed.
1. git log ->used to list the version history for the current branch.
   git log –follow[file] ->lists version history for a file, including the renaming of files also.
1. git show [commit] ->shows the metadata and content changes of the specified commit.
1. git tag [commitID] ->used to give tags to the specified commit.
1. git branch ->lists all the local branches in the current repository.
   git branch [branch name] -> creates a new branch.
   git branch -d [branch name] -> deletes the feature branch.
1. git checkout [branch name] -> used to switch from one branch to another
   git checkout -b [branch name] ->creates a new branch and also switches to it.
1. git merge [branch name] ->merges the specified branch’s history into the current branch.
1. git remote add [variable name] [Remote Server Link] ->used to connect your local repository to the remote server.
1. git push [variable name] master ->sends the committed changes of master branch to your remote repository.
   git push [variable name] [branch] ->sends the branch commits to your remote repository.
   git push –all [variable name] ->pushes all branches to your remote repository.
   git push [variable name] :[branch name] ->deletes a branch on your remote repository.
1. git pull [Repository Link] ->fetches and merges changes on the remote server to your working directory.
1. git stash save ->stores all the modified tracked files.
1. git stash pop ->restores the most recently stashed files.
   git stash list ->lists all stashed changesets.
   git stash drop ->discards the most recently stashed changeset.


































**SSH key:**

ssh-keygen -t rsa -b 4096 -C “user email”

name ( private key, not to be shared or uploaded )

name.pub ( Is the key you will upload to github


**Creating a SSH Key:**

-ssh-keygen -t rsa -b 4096 -C "email@example.com" // to create your set of keys both public and private key and save it into a file

-vim ~/.ssh/config // to open up the file you created which contains the keys

-[ Host \*

AddKeysToAgent yes



UserKeychain yes

IdentityFile ~/.ssh/id\_rsa ] // paste this line of code in the [ ] in the file you create after executing the vim ~/.ssh/config command

- ls | grep gitkey // to display the keys created
- cat key\_name // to display the content of any key created
- ssh-agent -s // to start the ssh-agent in the background
- vim ~/.ssh/config // to configure the created file which contains the keys
- ssh-add -K ~/.ssh/private\_key\_name // to add the private key to the ssh agent
  The above commands should help you setup your ssh keys properly

















