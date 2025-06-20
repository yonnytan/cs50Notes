# Terminal Commands for File Management and Git

## 📋 Table of Contents

- [📁 File Management Commands](#-file-management-commands)
- [🔧 Git Commands](#-git-commands)
  - [Basic Workflow](#basic-workflow)
  - [Repository Management](#repository-management)
  - [Branching and Merging](#branching-and-merging)
  - [History and Logs](#history-and-logs)

## 📁 File Management Commands

| Command | Description                                    | Examples                                                                                                                       | When Would I Use This?                                                                                                           |
| ------- | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| `ls`    | List files and directories in current location | `ls` - basic list<br>`ls -la` - detailed list with hidden files<br>`ls -lh` - human-readable file sizes                        | When you need to see what files are in your current directory, check if a file exists, or explore the contents of a folder       |
| `cd`    | Change directory                               | `cd Documents` - enter folder<br>`cd ..` - go back one level<br>`cd ~` - go to home directory<br>`cd /` - go to root directory | When you need to navigate to a different folder to work on files, access your project directory, or move around your file system |
| `touch` | Create new file(s)                             | `touch index.html`<br>`touch file1.txt file2.txt`<br>`touch "file with spaces.txt"`                                            | When you need to create empty files quickly, set up project structure, or create placeholder files before editing                |
| `mkdir` | Create new directory                           | `mkdir my-project`<br>`mkdir -p parent/child` - create nested directories                                                      | When starting a new project, organizing files into folders, or creating a directory structure for your code                      |
| `rm`    | Remove files/directories                       | `rm file.txt` - delete file<br>`rm -r folder/` - delete folder and contents<br>`rm -f file.txt` - force delete                 | When cleaning up old files, removing temporary files, or deleting entire project folders you no longer need                      |
| `cp`    | Copy files/directories                         | `cp source.txt destination.txt`<br>`cp -r folder/ new-folder/`                                                                 | When backing up files, creating duplicates for testing, or copying project templates to start new work                           |
| `mv`    | Move/rename files                              | `mv old-name.txt new-name.txt`<br>`mv file.txt folder/`                                                                        | When reorganizing your project structure, renaming files to follow naming conventions, or moving files to appropriate folders    |

## 🔧 Git Commands

### Basic Workflow

| Command                    | Description                                                                           | Examples                                                                                                                    | When Would I Use This?                                                                                                            |
| -------------------------- | ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `git clone [url]`          | Download repository to local machine                                                  | `git clone https://github.com/user/repo.git`<br>`git clone https://github.com/user/repo.git my-folder`                      | When you want to download an existing project from GitHub, contribute to open source, or start working with a team's codebase     |
| `git add [files]`          | Stage files for commit                                                                | `git add file.txt` - add specific file<br>`git add .` - add all changes<br>`git add *.js` - add all JavaScript files        | When you've made changes to files and want to prepare them for committing, selecting which changes to include in your next commit |
| `git commit -m "message"`  | Save staged changes with description                                                  | `git commit -m "Add new feature"`<br>`git commit -m "Fix bug in login"`                                                     | When you want to save your work with a meaningful description, creating a checkpoint in your project's history                    |
| `git push`                 | Upload commits to remote repository                                                   | `git push` - push to current branch<br>`git push origin main` - push to specific branch                                     | When you want to share your local changes with others, backup your work to GitHub, or deploy your code                            |
| `git pull`                 | Download latest changes from remote                                                   | `git pull` - pull from current branch<br>`git pull origin main` - pull from specific branch                                 | When working with others and need to get their latest changes, or when you've made changes on GitHub and need them locally        |
| `git status`               | Check current repository status                                                       | `git status` - see what's staged/changed<br>`git status --porcelain` - machine-readable output                              | When you want to see what files you've changed, what's ready to commit, or understand the current state of your repository        |
| `git commit -am "message"` | Stage and commit all tracked files <br> (mixes git add . and git commit -m 'message') | `git commit -am "Quick fix"` - add and commit modified files<br>`git commit -am "Update documentation"` - skip staging step | When you want to quickly commit changes to files that Git is already tracking, saving time by skipping the separate add step      |

### Repository Management

| Command                       | Description                   | Examples                                                                                              | When Would I Use This?                                                                                             |
| ----------------------------- | ----------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| `git init`                    | Initialize new Git repository | `git init` - create repo in current directory<br>`git init my-project` - create repo in new directory | When starting a new project from scratch and want to begin tracking changes with Git                               |
| `git remote add origin [url]` | Connect local repo to remote  | `git remote add origin https://github.com/user/repo.git`                                              | When you've created a local repository and want to connect it to a GitHub repository for backup and collaboration  |
| `git remote -v`               | View remote repositories      | `git remote -v` - shows all remotes and URLs                                                          | When you want to check which remote repositories your local repo is connected to, or verify the correct GitHub URL |

### Branching and Merging

| Command                 | Description                         | Examples                                                                         | When Would I Use This?                                                                                                                                |
| ----------------------- | ----------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git branch`            | List all branches                   | `git branch` - local branches<br>`git branch -a` - all branches (local + remote) | When you want to see what branches exist in your project, or check which branch you're currently on                                                   |
| `git branch [name]`     | Create new branch                   | `git branch feature-login`<br>`git branch -d old-branch` - delete branch         | When you want to work on a new feature without affecting the main code, or clean up old branches you no longer need                                   |
| `git checkout [branch]` | Switch to different branch          | `git checkout main`<br>`git checkout -b new-feature` - create and switch         | When you want to switch between different features you're working on, or move back to the main branch                                                 |
| `git merge [branch]`    | Combine changes from another branch | `git merge feature-branch`<br>`git merge --abort` - cancel merge                 | When you've finished working on a feature and want to integrate it into the main branch, or when you need to combine work from different team members |

### History and Logs

| Command    | Description                       | Examples                                                                                                                  | When Would I Use This?                                                                                                                               |
| ---------- | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git log`  | View commit history               | `git log` - full history<br>`git log --oneline` - compact view<br>`git log -n 5` - last 5 commits                         | When you want to see what changes have been made to your project, find when a bug was introduced, or understand the project's development history    |
| `git diff` | See changes between commits/files | `git diff` - unstaged changes<br>`git diff --staged` - staged changes<br>`git diff HEAD~1` - compare with previous commit | When you want to review what you've changed before committing, compare different versions of your code, or understand what a specific commit changed |

### Advanced Commands

| Command      | Description                              | Examples                                                                                                               | When Would I Use This?                                                                                                                      |
| ------------ | ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `git stash`  | Temporarily save changes                 | `git stash` - save current changes<br>`git stash pop` - restore saved changes<br>`git stash list` - view saved stashes | When you need to switch branches but have uncommitted changes, or when you want to temporarily save work in progress to try something else  |
| `git reset`  | Undo commits or unstage files            | `git reset HEAD~1` - undo last commit<br>`git reset --hard HEAD~1` - undo commit and changes                           | When you made a mistake in your last commit and want to undo it, or when you want to unstage files you accidentally added                   |
| `git rebase` | Reapply commits on top of another branch | `git rebase main` - rebase current branch onto main                                                                    | When you want to keep your feature branch up-to-date with the latest changes from main, or when you want to create a cleaner commit history |

### Merge Conflict

| Command          | Description               | Examples                                   | When Would I Use This?                                                                                              |
| ---------------- | ------------------------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| `git status`     | Check for merge conflicts | `git status` - shows conflicted files      | When you're in the middle of a merge and want to see which files have conflicts that need to be resolved            |
| `git diff`       | View conflict markers     | `git diff` - shows conflict areas in files | When you want to see exactly what the conflicts are in your files, helping you understand what needs to be resolved |
| `git add [file]` | Mark conflict as resolved | `git add conflicted-file.txt`              | When you've manually resolved conflicts in a file and want to tell Git the conflict is fixed                        |
| `git commit`     | Complete the merge        | `git commit` - creates merge commit        | When all conflicts are resolved and you want to finalize the merge process                                          |

## ⛙ Understanding Merge Conflicts

### What Are Merge Conflicts?

Merge conflicts occur when Git cannot automatically merge changes because the same parts of a file have been modified in different ways on different branches. This commonly happens when:

- Two people edit the same line of code
- One person edits a file while another person deletes it
- Two people add different content to the same location in a file

---

### How Merge Conflicts Happen

1. **Same File, Different Changes**: Two branches modify the same lines of code
2. **Divergent History**: Branches have evolved independently with overlapping changes
3. **Conflicting Operations**: One branch adds content while another deletes the same area

---

### Common Scenarios

| Scenario                        | Description                                | Example                                                  |
| ------------------------------- | ------------------------------------------ | -------------------------------------------------------- |
| **Line-level conflicts**        | Same lines modified differently            | Both branches change the same function name              |
| **File deletion conflicts**     | One branch deletes, other modifies         | Branch A deletes `config.js`, Branch B updates it        |
| **Content insertion conflicts** | Both branches add content at same location | Both branches add different imports at the top of a file |

---

### How to Resolve Merge Conflicts

#### Step 1: Identify Conflicts

When Git encounters a merge conflict, it marks the conflicting sections in your files using conflict markers like this:

```plaintext
<<<<<<< HEAD
Your changes on the current branch
Example: <h1>Hello World</h1>
=======
Incoming changes from the branch you're merging
Example: <h1 style="color:blue">Hello World!!!</h1>
>>>>>>> feature-branch
```

These markers help you see exactly what parts are in conflict between the two versions of the file.

#### Step 2: Manually Edit the File

Go through each marked conflict and decide which changes to keep. You have three options:

- Keep your version
- Keep the incoming version
- Combine both manually

After editing, remove the conflict markers (<<<<<<<, =======, >>>>>>>) from the file.

#### Step 3: Mark as Resolved

Once you've finished resolving all conflicts in a file: <br>
`git add <filename>`<br>
Repeat this for every conflicted file.

#### Step 4: Complete the Merge

Once all conflicts are resolved and added:<br>
`git commit`<br>
Git may auto-generate a commit message for the merge. You can edit it or leave it as is.
