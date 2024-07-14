### 1. **Tracking Changes**

- **Checking Status:** Use `git status` to see the current state of your repository, including which files are modified, staged, or untracked:

  ```
  git status
  ```

- **Viewing Differences:** Use `git diff` to see the differences between the working directory and the staging area:
  ```
  git diff
  ```
  To compare the differences between the staging area and the last commit, use:
  ```
  git diff --cached
  ```

### 2. **Staging Changes**

- **Adding Changes:** Use `git add` to stage specific files or changes for the next commit:

  ```
  git add filename.txt
  ```

  To add all changes in the current directory and its subdirectories, use:

  ```
  git add .
  ```

- **Removing Changes from Staging:** Use `git reset` to unstage files while keeping the changes in the working directory:
  ```
  git reset filename.txt
  ```

### 3. **Committing Changes**

- **Committing:** Use `git commit` to commit staged changes to the repository with a descriptive message:

  ```
  git commit -m "Add new feature"
  ```

- **Amending the Last Commit:** If you need to modify the last commit (e.g., to add forgotten files or fix a typo in the message), use `git commit --amend`:
  ```
  git commit --amend
  ```

### 4. **Viewing History**

- **Viewing Commit History:** Use `git log` to view a list of commits in reverse chronological order:

  ```
  git log
  ```

- **Viewing Detailed Commit Information:** To see details of each commit (including changes), use `-p` option:
  ```
  git log -p
  ```

### 5. **Undoing Changes**

- **Discarding Changes:** Use `git checkout -- filename.txt` to discard changes in the working directory (before staging):

  ```
  git checkout -- filename.txt
  ```

- **Unstaging Changes:** Use `git reset HEAD filename.txt` to unstage changes (after staging but before committing):

  ```
  git reset HEAD filename.txt
  ```

- **Undoing Commits:** Use `git revert <commit-hash>` to create a new commit that undoes the changes made in a specific commit:

  ```
  git revert abcdef123456
  ```

- **Resetting to a Previous Commit:** Use `git reset --hard <commit-hash>` to reset the repository to a specific commit, discarding all changes made after that commit:
  ```
  git reset --hard abcdef123456
  ```

### 6. **Resolving Merge Conflicts**

- **Viewing Conflicts:** When merging branches, Git may encounter conflicts. Conflicting files will contain conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`). Resolve conflicts manually in these files.

- **Committing Resolved Conflicts:** After resolving conflicts, stage the resolved files and commit the merge:
  ```
  git add filename.txt
  git commit -m "Merge branch 'branch-name'"
  ```

### 7. **Stashing Changes**

- **Stashing:** Use `git stash` to temporarily store changes that are not ready to be committed:

  ```
  git stash
  ```

- **Applying Stashed Changes:** Use `git stash apply` to re-apply stashed changes to the working directory:
  ```
  git stash apply
  ```

### 8. **Ignoring Files**

- **Ignoring Files:** Create a `.gitignore` file in the root of your repository to specify files and directories that Git should ignore. Each line in `.gitignore` specifies a pattern to match files/directories:
  ```
  *.log
  build/
  ```

### Conclusion

Understanding how to effectively manage changes in Git is crucial for maintaining a clear and organized development workflow. By mastering these commands and practices, you can efficiently track modifications, collaborate with others, and ensure the integrity of your project's version history. Practice and familiarity with Git's capabilities will further enhance your ability to handle various scenarios that arise during software development.
