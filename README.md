# Git Guidelines: From Basic to Advanced

Welcome to the Git Guidelines! This document covers the essentials of Git, from basic commands to advanced practices, ensuring a smooth and productive experience for version control and collaboration.

## Table of Contents

1. [Introduction](#introduction)
2. [Setup and Configuration](#setup-and-configuration)
3. [Basic Git Commands](#basic-git-commands)
4. [Branching Strategies](#branching-strategies)
5. [Working with Remotes](#working-with-remotes)
6. [Collaboration and Pull Requests](#collaboration-and-pull-requests)
7. [Stashing and Rebasing](#stashing-and-rebasing)
8. [Resolving Merge Conflicts](#resolving-merge-conflicts)
9. [Advanced Git Commands](#advanced-git-commands)
10. [Best Practices](#best-practices)
11. [Common Issues and Troubleshooting](#common-issues-and-troubleshooting)
12. [References and Resources](#references-and-resources)

---

## 1. Introduction

Git is a distributed version control system that allows teams to collaborate efficiently on projects. It helps in tracking changes, managing code versions, and supporting branching strategies for feature development and bug fixes.

---

## 2. Setup and Configuration

### Install Git

Download Git from [git-scm.com](https://git-scm.com) and install it on your system.

### Configure User Information

Set up your name and email, which will appear in commit history:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Verify Configuration

```bash
 git config --list

```

## 3. Basic Git Commands

### Initializing a Repository

```bash
 git init
```

### Cloning a Repository

```bash
git clone <repository-url>
```

### Checking Repository Status

```bash
 git status
```

### Adding Changes

```bash
 git add <file>       # Add a specific file
 git add .            # Add all changes

```

### Committing Changes

```bash
git commit -m "Commit message"
```

### Viewing Commit History

```bash
git log
```

### Undoing Changes

```bash
git checkout -- <file>   #Discard unstaged changes
git reset <file>         #Unstage a file
```

## 4. Branching Strategies

### Creating a Branch

```bash
git branch <branch-name>

```

### Switching to a Branch

```bash
git checkout <branch-name>
```

### Creating and Switching Simultaneously

```bash
 git checkout -b <branch-name>
```

### Deleting a Branch

```bash
git branch -d <branch-name>

```

## 5. Working with Remotes

### Adding a Remote

```bash
git remote add origin <repository-url>
```

### Fetching Changes

```bash
 git fetch origin

```

### Pushing Changes

```bash
git push origin <branch-name>

```

## 6. Collaboration and Pull Requests

### Pull Request Workflow

1.Create a feature branch.
2.Push changes to the remote.
3.Open a pull request on the repository.
4.Request reviews and address feedback.
5.Merge the pull request once approved.

## 7. Stashing and Rebasing

### Stashing Changes

```bash
git stash
```

### Applying Stashed Changes

```bash
  git stash apply
```

### Rebasing a Branch

```bash
  git rebase <base-branch>
```

## 8. Resolving Merge Conflicts

1.Identify conflicts using git status.
2.Open conflicting files and resolve issues.
3.Mark as resolved

```bash
git add <file>
```

4.Continue with the merge

```bash
git merge --continue
```

## 9. Advanced Git Commands

### Reverting a Commit

```bash
git revert <commit-hash>
```

### Cherry-picking a Commit

```bash
git cherry-pick <commit-hash>
```

### Squashing Commits

```bash
git rebase -i HEAD~<number-of-commits>
```

## 10. Best Practices

### Use descriptive messages

### Branch Naming

Follow a consistent pattern.

- Example
  -feature/add-login
  -fix/user-authentication

### Small, Frequent Commits

- Avoid large commits; commit changes frequently.

### Code Reviews

- Always request and perform code reviews before merging.

### Backup Work

- Push changes to a remote regularly.

## 11. Common Issues and Troubleshooting

### Detached HEAD State

-Resolve by checking out a branch

```bash
 git checkout <branch-name>
```

### Recovering Deleted Branches

```bash
git reflog
git checkout -b <branch-name> <commit-hash>

```

### Undoing Last Commit

```bash
git reset --soft HEAD~1
```

## 12. References and Resources

- [Git Official Documentation](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
