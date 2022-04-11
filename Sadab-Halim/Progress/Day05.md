# Linux

### Debian Packaging
dpkg is the underlying package manager for these systems. It can instal, remove, and build packages. Unlike higher-level package management systems.

Package Management in the Debain Family System

For Debian-based systems, the higher-level package management system is the Advanced Package Tool (APT) system of utilities.

### Red Hat Package Manager (RPM)
Red Hat Package Manager (RPM) is the other package management system popular linux distributions. It was developed by Red Hat, and adopted by a number of other disttibutions, including SUSE/openSUSE, Mageia, CentOS, Oracle Linux, and others.

### openSUSE's YaST S oftware Mangement
The Yet another Setup Tool (YaST) software manager is similar to other graphical package managers. It is an RPM-based application.

### VI Editor
VI Editor has two modes of operations: 
- Command Mode
- Insert Mode

When we open a file in VI Editor by default we are in **Command Mode**.
In the **Command Mode** we can issue commands to the editor such as to copy and paste lines, delete lines or to naviage between lines, etc. But we cannot write content to the file in Command Mode.

To write contents to the file we must switch to **Insert Mode**.

_To Switch to Insert Mode_, type `i`

Now, we can modify the modify the file content as per our wish.

_To switch back to Command Mode from Insert Mode_, press `Esc`

### VI Editor Command Mode

![image](https://user-images.githubusercontent.com/74575612/150750561-e30121c6-bbab-4f2c-bd61-df384c52c514.png)

![image](https://user-images.githubusercontent.com/74575612/150750659-a0287b61-00e9-4798-8020-3b024c72714d.png)

- `/` to find in the text editor, for example if we want to find _of_ then, we will write the command as `/of`

To move the cursor to the rest of occurences in find, press `n` key.

# Git

### Git Cheat Sheet

**Setup:** Configuring user information used across all local repositories

- `git config --global user.name "[your_name]"` set a name 
- `git config --global user.email "[your_email]"` set an email address

**Setup & INIT:** Configuring user information, initializing and cloning repositories

- `git init` initialize an existing directory as a Git repository
- `git clone [url]` retrieve an entire repository from a hosted location via URL

**Stage & SnapShot:** Working with snapshots and the Git staging area

- `git status` show modified files in working directory, staged for your next commit
- `git add [file]` add a file as it looks now to your next commit (stage)
- `git reset [file]` unstage a file while retaining the changes in working directory
- `git diff` diff of what is changed but not staged
- `git diff --staged` diff of what is staged but not yet committed
- `git commit -m "[descriptive message]"` commit your staged content as a new commit snapshot

**Branch & Merge:** Isolating work in branches, changing context, and interchanging changes

- `git branch` list your branches. a*will appear next to the currently active branch
- `git branch [branch-name]` create a new branch at the current commit
- `git checkout` switch to another branch and check it out into the current one
- `git merge [branch]` merge the specified branch's history into the current one
- `git log` show all commits in the current branch's history

**Inspect & Compare:** Examining logs, diffs and object information

- `git log` show the commit history for the currently active branch
- `git log branchB..branchA` show the commits on branchA that are not on branchB
- `git log --follow [file]` show the commits that changed file, even across renames
- `git diff branchB..branchA` show the diff of what is in branchA that is not in branchB
- `git show [SHA]` show any object in Git in human-readable format

**Tracking Path Changes:** Versioning file removes and path changes

- `git rm [file]` delete the file from project and stage the removal for commit
- `git mv [existing-path] [new-path]` change an existing file path and stage the move
- `git log --start -M` show all commit logs with indication of any paths that moved

**Share & Update:** Retrieving updates from another repository and updating local repos

- `git remote add [alias] [url]` add a git URL as an alias
- `git fetch [alias]` fetch down all the branches form that Git remote
- `git merge [alias]/[branch]`merge a remote branch into your current branch to bring it up to date
- `git push [alias] [branch]` transmit local branch commits to the remote repository branch
- `git pull` fetch and merge any commits from the tracking remote branch

**Rewrite History:** Rewriting branches, updating commits and clearing history

- `git rebase [branch]` apply any commits of current branch ahead of specified one
- `git reset --hard [commit]` clear staging area, rewrite working tree from specfied commit

**Temporary Commits:** Temporarily store modified, tracked files in order to change branches

- `git stash` save modified and staged changes
- `git statsh list` list stack-order of staged file changes
- `git stash pop` write working from top of stash stack
- `git stash drop` discard the changes from top of stash stack

**Ignoring Patterns:** Preventing unintentional staging or commiting of files

- `log/
   *.notes
   pattern*/`
   save a file with desired pattern as .gitignore with either direct string matches or wildcard globs.

- `git config --global core.excludefile [file]` system wide ignore patterm for all local repositories


Resources:
- [Introductiont to Linux](https://www.edx.org/course/introduction-to-linux)
- [DevOps Prerrequisite Course](https://www.youtube.com/watch?v=Wvf0mBNGjXY)
- [Complete Git and Github Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics)
