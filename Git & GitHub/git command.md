# Cheat Sheet
## SETUP

+ Set a name that is identifiable for credit when review version history
```bash
git config --global user.name "[firstname lastname]"
```

+ Set a email address that will be associated with each history marker
```bash
git config --global user.email "[valid-email]"
```

+ Set automatic command line coloring for Git for easy reviewing
```bash
git config --global color.ui auto
```

## SETUP & INIT

+ Initialize an existing directory as a Git repository
```bash
git init
```

+ Retrieve an entire repository from a hosted location via URL
```bash
git clone [url]
```

## STAGE & SNAPSHOT

+ Show modified files in working directory, staged for your next commit
```bash
git status
```

+ Add a file as it looks now to your next commit (stage)
```bash
git add [file]
```

+ Add all files in the staging area
```bash
git add .
or
git add -A
or 
git add *
```

+ Unstage a file while retaining the changes in working directory
```bash
git reset [file]
```

+ Diff of what is changed but not staged
```bash
git diff
```

+ Diff of specific file
```bash
git diff filename.py
```

+ Diff of what is staged but not yet committed
```bash
git diff --staged
```

+ Commit your staged content as a new commit snapshot
```bash
git commit -m "[description message]"
```

+ Commit changes and skip the staging area
```bash
git commit -a -m "[description message]"
```

## BRANCH & MERGE

+ List your branches. a * will appear next to the currently active branch
```bash
git branch
```

+ Create a new branch at the current commit
```bash
git branch [branch-name]
```

+ Switch to another branch and check it out into your working directory
```bash
git checkout [branch-name]
```

+ Merge the specified branch's history into the current one
```bash
git merge [branch]
```

+ Deletes the specified branch
```bash
git branch -d [branch-name]
```

+ Show all commits in the current branch's history
```bash
git log
```

## INSPECT & COMPARE

+ Show the commit history for the current active branch
```bash
git log
```

+ See your commit history including changes in Git
```bash
git log -p
```

+ See log stats in Git
```bash
git log --stat
```

+ Show commit log as a graph 
```bash
git log --graph --oneline
```

+ Show the commit on branchA that are not on branchB
```bash
git log branchB..branchA
```

+ Show the commits that changed file, even across renames
```bash
git log --follow [file]
```

+ Show the diff of what is in branchA that is not in branchB
```bash
git diff branchB...branchA
```

+ Show any object in Git in human-readable format
```bash
git show [SHA]
```

+ See a specific commit
```bash
git show [commit-id]
```

## SHARE & UPDATE

+ Add a git URL as an alias
```bash
git remote add [alias] [url]
```

+ Fetch down all the branches from that Git remote
```bash
git fetch [alias]
```

+ Merge a remote branch into your current branch to bring it up to date
```bash
git merge [alias]/[branch]
```

+ Transmit local branch commits to the remote repository branch
```bash
git push [alias] [branch]
```

+ Fetch and merge any commits from the tracking remote branch
```bash
git pull
```

## TRACKING PATH CHANGES

+ Delete the file from project and stage the removal for commit
```bash
git rm [file]
```

+ Change an existing file path and stage the move
```bash
git mv [existing-path] [new-path]
```

+ Show all commit logs with indication of any paths that moved
```bash
git log --stat -M
```

## REWRITE HISTORY

+ Apply any commits of current branch ahead of specified one
```bash
git rebase [branch]
```

+ Undoes all commits after commit, preserving changes locally
```bash
git reset [commit]
```

+ Clear staging area, rewrite working tree from specified commit
```bash
git reset --hard [commit]
```

## TEMPORARY COMMITS

+ Save modified and staged changes
```bash
git stash
```

+ List stack-order of stashed file changes
```bash
git stash list
```

+ Write working from top of stash stack
```bash
git stash pop
```

+ Discard the changes from top of stash stack
```bash
git stash drop
```

## REMOTE REPO

+ Add remote repository
```bash
git add remote "[URL]"
```

+ See remote URL
```bash
git remote -v
```

+ Get more info about a remote repo
```bash
git remote show origin
```



