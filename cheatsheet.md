# `GitHub Git Cheat Sheet`

![Image](/images/screenshot_github_cheat-sheet.png "Credits: GitHub, Inc. @ www.github.com")

Git is the free and open source distributed version control system that’s responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

## `INSTALLATION & GUIS`

**With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.**

`GitHub for Windows`

[https://windows.github.com](https://windows.github.com)

`GitHub for Mac`

[https://mac.github.com](https://mac.github.com)

> **For Linux and Solaris platforms, the latest release is available on the official Git web site.**

`Git for All Platforms`

[http://git-scm.com](http://git-scm.com)

## `SETUP * CONFIGURE TOOLING`

**Configuring user information used across all local repositories**

    $ git config --global user.name "[firstname lastname]"

Set a name that is identifiable for credit when review version history

    $ git config --global user.email "[valid email]"

Set an email address that will be associated with each history marker

    $ git config --global color.ui auto

Set automatic command line coloring for Git for easy reviewing

## `INIT * CREATE REPOSITORIES`

**A new repository can either be created locally, or an existing repository can be cloned. When a repository was initialized locally, you have to push it to GitHub afterwards.**

    $ git init

The git init command turns an existing directory into a new Git repository inside the folder you are running this command. After using the git init command, link the local repository to an empty GitHub repository using the following command:

    $ git remote add origin [url]

Specifies the remote repository for your local repository. The url points to a repository on GitHub.

    $ git clone [url]

Retrieve or clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits

## `THE .GITIGNORE FILE`

> **Sometimes it may be a good idea to exclude files from being tracked with Git. This is typically done in a special file named .gitignore. You can find helpful templates for .gitignore files at [github.com/github/gitignore](https://github.com/github/gitignore).**

## `SYNCHRONIZE CHANGES`

**Synchronize your local repository with the remote repository on GitHub.com**

    $ git fetch

Downloads all history from the remote tracking branches

    $ git merge

Combines remote tracking branches into current local branch

    $ git push

Uploads all local branch commits to GitHub

    $ git pull

Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. git pull is a combination of git fetch and git merge

## `BRANCHES`

**Isolating work in branches, changing context, and integrating changes git branch list your branches. a * will appear next to the currently active branch: Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to. Use git status to see which branch that is.**

    $ git branch [branch-name]

Creates a new branch

    $ git checkout

Switch to another branch and check it out into your working directory

    $ git switch -c [branch-name]

Switches to the specified branch and updates the working directory

    $ git merge [branch]

Merges or combines the specified branch’s history into the current branch. This is usually done in pull requests, but is an important Git operation.

    $ git branch -d [branch-name]

Deletes the specified branch

## `STAGE & SNAPSHOT`

**Working with snapshots and the Git staging area git status show modified files in working directory, staged for your next commit**

    $ git add [file]

Add a file as it looks now to your next commit (stage)

    $ git reset [file]

Unstage a file while retaining the changes in working directory

    $ git diff

Diff of what is changed but not staged

    $ git diff --staged

Diff of what is staged but not yet committed

    $ git commit -m "[descriptive message]"

Commit your staged content as a new commit snapshot

## `LOG`

*Browse and inspect the evolution of project files*

    $ git log

Show all commits in the current branch’s history

    $ git log

Lists version history for the current branch

    $ git log --follow [file]

Lists version history for a file, beyond renames (works only for a single file)

## `INSPECT & COMPARE`

**Examining logs, diffs and object information git log show the commit history for the currently active branch**

    $ git log [first-branch]..[second-branch]

Show the commits on first-branch that are not on second-branch

    $ git log --follow [file]

Show the commits that changed file, even across renames

    $ git diff [first-branch]...[second-branch]

Shows content differences between two branches

    $ git show [commit]

Outputs metadata and content changes of the specified commit

    $ git show [SHA]

Show any object in Git in human-readable format

## `TRACKING PATH CHANGES`

**Versioning file removes and path changes**

    $ git rm [file]

Delete the file from project and stage the removal for commit

    $ git mv [existing path] [new path]

Change an existing file path and stage the move

    $ git log --stat -M

Show all commit logs with indication of any paths that moved

## `IGNORING PATTERNS`

**Preventing unintentional staging or committing of files**

    logs/
    *.notes
    pattern*/

Save a file with desired patterns as .gitignore with either direct string matches or wildcard globs.

    $ git config --global core.excludesfile [file]

System wide ignore pattern for all local repositories

## `SHARE & UPDATE`

**Retrieving updates from another repository and updating local repos**

    $ git remote add [alias] [url]

Add a git URL as an alias

    $ git fetch [alias]

Fetch down all the branches from that Git remote

    $ git merge [alias]/[branch]

Merge a remote branch into your current branch to bring it up to date

    $ git push [alias] [branch]

Transmit local branch commits to the remote repository branch

    $ git pull

Fetch and merge any commits from the tracking remote branch: Updates your current local working branch with all new commits from the corresponding remote branch on     GitHub. git pull is a combination of git fetch and git merge

## `REWRITE HISTORY * REDO COMMITS`

**Rewriting branches, updating commits and clearing history**

> CAUTION! Changing history can have nasty side effects. If you need to change commits that exist on GitHub (the remote), proceed with caution. If you need help, reach out at github.community or contact support.

    $ git rebase [branch]

Apply any commits of current branch ahead of specified one

    $ git reset [commit]

Undoes all commits after [commit], preserving changes locally

    $ git reset --hard [commit]

Clear staging area, rewrite working tree from specified commit

## `TEMPORARY COMMITS`

**Temporarily store modified, tracked files in order to change branches**

    $ git stash

Save modified and staged changes

    $ git stash list

List stack-order of stashed file changes

    $ git stash pop

Write working from top of stash stack

    $ git stash drop

Discard the changes from top of stash stack

## `Glossary`

- git: an open source, distributed version-control system
- GitHub: a platform for hosting and collaborating on Git repositories
- commit: a Git object, a snapshot of your entire repository compressed into a SHA
- branch: a lightweight movable pointer to a commit
- clone: a local version of a repository, including all commits and branches
- remote: a common repository on GitHub that all team members use to exchange their changes
- fork: a copy of a repository on GitHub owned by a different user
- pull request: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more
- HEAD: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git switch

----

© 2022 GitHub, Inc.
























