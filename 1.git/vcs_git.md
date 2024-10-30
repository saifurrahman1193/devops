### VCS (version control system)
-  tool that helps manage and track changes in code and maintain history of the changes, documents, or other digital files over time

### Git
- one of VCS
- there are others VCS like git
- collaboration tool among developers
- repository sytem

### GitHub
- server where can i store code

### Git Setup & Configuration
#### Username and email setup

```
git config
git config -l
git config --global user.name "saifurrahman1193"
git config --global user.email "saifur.rahman1193@gmail.com"
```

#### Basic commands
```
git init
git init --help
ls 
ls -a
touch file.txt

```

- add (means to track the file)

```
git init
git add .
git commit -m "first commit"
git status
git branch
git checkout branch
```



### git init
  - Initializes a new Git repository in the current directory. 
  - This command creates a .git folder where Git stores version history.


### .git folder
  - containing all information, history, and settings for managing and tracking changes to your files
  - It's like a DB
  - Key Contents
    1. HEAD
    2. config
    3. index
    4. hooks/
    5. logs/
    6. objects/
    7. refs/
    8. packed-refs

### git add
- Stages Changes: Prepares changes for a commit by adding them to the staging area.
- Selective Staging: You can stage individual files or specific portions of files.
- Common Commands:
  - Add a Specific File: ```git add <file-name>```
  - Add All Changes in Directory:```git add .```
  - Add Specific Directory: ```git add <directory-name>```

Required Before Commit: Changes must be added to the staging area with git add before they can be committed.


### Commit
- Meaningful, must be present sentence not past sentence
- Snapshot of Changes: A commit records all staged changes in the project.
- Unique ID (SHA-1 Hash): Each commit is uniquely identified by a hash, making it easy to track and reference.
- Commit Message: A message describing what changes were made, added with the -m flag (e.g., git commit -m "Description").
- Building Project History: Each commit builds on the previous, creating a timeline of changes.
- must be added first (tracking)
- after commit files goes from staging environment then move changes  to the repositoryvc
- mainly save the files

Key Command:

```
git commit -m "commit message"
```
Amending a Commit: You can modify the last commit with git commit --amend (useful for updating messages or adding files).


#### GIT commit types
```
feat: New feature for the user.
fix: Bug fix.
style: Code Style Changes.
refactor: Code Refactoring.
build: Build System Changes.
ci: Continuous Integration Changes.
perf: Performance Improvements.
revert: Revert a Previous Commit.
docs: Documentation changes.
test: Adding or modifying tests.
chore: Routine tasks, maintenance, or housekeeping.
```



### Branch
- Branches allow isolated work on features, fixes, or experiments.
- tree root
```
git branch

```

### checkout

- Switch Branches: Changes the current branch to another existing branch.
  ```
    git checkout <branch-name>
  ```
- Create and Switch to a New Branch:
    ```
    git checkout -b <new-branch-name>
    ```

- Restore Files: Replaces changes in the working directory with the version from the last commit, or from a specified commit.
    ```
    git checkout <file-name>
    ```

    This will discard any uncommitted changes in that file.

- Detached HEAD State:

    If you checkout a specific commit (not a branch), Git enters a "detached HEAD" state, where HEAD points directly to that commit. Changes made in this state won't be associated with any branch unless a new branch is created

### head
- Tracks the Current Position: HEAD points to the most recent commit in your current branch.
- has an address

### staging
- after use ```git add file_name or folder_name or (.)```
- Staging Area: A temporary space that holds changes you plan to commit.
- Selective Commits: You can choose specific changes to include in each commit by staging only certain files or portions of files.
- Staging Changes: Use git add to add changes to the staging area.
- Viewing Staged Changes: Use git status to see which changes are staged vs. unstaged.
- Making a Commit: Once staged, you commit the changes with git commit, which moves them from the staging area to the repository’s history.

