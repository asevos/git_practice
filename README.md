# Git practice for production

This repository contains some tasks to practice Git usage in CLI (minimal production toolkit). Some Git knowledge is expected for this practice so it won't be suitable to learn the basics.

## About

This is a set of tasks that aims to help you prepare for production projects Git management. You'll need to search how to perform these tasks by yourself but each task would contain hints, guiding your search.

It is expected that you have basic Git knowledge and know what is a branch, a remote, a commit, a commit message and a commit hash. 

This set of tasks is designed with Git bash in mind and aims to train you using CLI. However it shouldn't be a problem to complete all the tasks with any GUI (but we all know that CLI is the *truest* way).

So hope you enjoy and may StackOverflow be with you. 

## Tasks

- Do tasks in order to make sure that nothing breaks. 
- Try to avoid checking out into remote branches and train to use them without creating a local copy.

### 1. Take a look around

Make Git show you a list of branches in this repository. You should be able to use a Git command to see all / only local / only remote branches.

### 2. Look into branch history

To complete some tasks you'll need to find commit hashes by commit message. So for this task make Git show you the history of commits for all branches. 

<details><summary>Try this as well</summary>

Console output may be simplified to show all info for a commit on one line. You can also get output formed as a graph.

</details>

### 3. Branch out of a given commit
For this task find a commit with message "Added settings". Create a new branch called `result` from this commit.

<details><summary>Hint</summary>

You'll need to look up for commit hash and use it. You should've been able to look up commit hashes in task #2.

</details>

### 4. Check your code

Git has a command to check how much any two commits differ from each other. This and all following tasks would have commit hashes of expected `result` branch state. Using this tool you should be able to tell that your branch has expected file state. 

Expected result (commit hash): `71fb9cd`

### 5. Edit and commit

Open file `some_settings.json` and sort lines with settings in it alphabetically (a to z). Commit these changes. 

Expected result (commit hash): `d40b830`

### 6. Resolving merge conflicts

Merge branch `new_settings` into your branch `result`.
The goal here is to preserve logic from both changes to file `some_settings.json`. In the end, it should both:
- have new lines, added on `new_settings` branch;
- be sorted alphabetically (a to z). 

Expected result (commit hash): `898e7df`

### 7. Merge in a commit without it's history

Find a commit with message "Created first good file" and merge it's changes into your branch `result`. No changes from any other commit should be merged in. 

Expected result (commit hash): `da18ec0`

<details><summary>Hint</summary>

Don't use `git merge` because it merges commit and all it's history. But you only need changes from a commit without previous commits. Git has a special command to do this.

</details>

### 8. Copy a file from another branch

There is a file `./folder/good_file_b.txt` on branch `files`. It was added in a commit with another file that you don't need on your `result` branch. Copy that file using a Git command. 

Expected result (commit hash): `c71d7fe`

<details><summary>Hint</summary>

You'll need to use a command that you've already used but with right arguments. Commit messages and hashes don't matter, only branch name and path to file. 

</details>

### 9. Merge all your changes into branch `final` as one commit

For this task you'll need to use a technique called squashing commits. Switch to branch `final` and merge all changes from `result` as one big commit. Try to avoid rebasing.

Expected result should be the same as branch `expected`.

## What's next

Congratulations on completing these tasks, hope they were helpful in learning Git!

There are still many topics not covered this practice repository. I really recommend that you learn and practice following:
- unstaging changes
- using `git reset`
- amending commits
- how `git fetch` and `git pull` work
- difference between `git add .` and `git add -a`
- using local and global config