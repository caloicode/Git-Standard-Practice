# GitHub Standard Practice 🚀

This repository serves as my personal guide for setting up a GitHub repository with standard practices.

---

## 📌 Steps to Initialize and Push to GitHub

1. **Initialize Git in the directory**

   ```sh
   git init
   ```

   This creates a new Git repository in the current folder.

2. **Add all files to staging area**

   ```sh
   git add .
   ```

   Stages all changes (new files, modifications, deletions) for commit.

3. **Check the status**

   ```sh
   git status
   ```

   Shows which files are staged, unstaged, or untracked.

4. **Commit the changes**

   ```sh
   git commit -m "initial commit"
   ```

   Saves the changes in the repository with a commit message.

5. **Add remote repository**

   ```sh
   git remote add origin <github_repo_link>
   ```

   Links the local repository to the remote GitHub repository.

6. **Push the changes to GitHub**

   ```sh
   git push -u origin master
   ```

   Uploads the committed changes to the `master` branch of the remote repository.

---

## 🔄 Reverting Back to a Previous Commit

### 1. Soft Reset (Keep changes but reset commit history)

```sh
git reset --soft HEAD~1
```

Moves back one commit, but keeps all the changes staged.

### 2. Mixed Reset (Unstage changes but keep them in the working directory)

```sh
git reset --mixed HEAD~1
```

Moves back one commit and unstages changes, but the file modifications remain.

### 3. Hard Reset (Completely remove commit and changes)

```sh
git reset --hard HEAD~1
```

Moves back one commit and removes all changes permanently. **Use with caution!**

### 4. Revert (Create a new commit that undoes changes)

```sh
git revert HEAD
```

This creates a new commit that negates the changes from the last commit, preserving history.

---

## 🌿 Working with Branches

### 1. Create a New Branch

```sh
git branch <branch_name>
```

Creates a new branch but does not switch to it.

### 2. Switch to a Branch

```sh
git checkout <branch_name>
```

Switches to the specified branch.

### 3. Create and Switch to a New Branch

```sh
git checkout -b <branch_name>
```

Creates a new branch and switches to it immediately.

### 4. Push a Branch to Remote

```sh
git push -u origin <branch_name>
```

Pushes the newly created branch to the remote repository.

### 5. Merge a Branch into Main

```sh
git checkout master
git merge <branch_name>
```

Merges the specified branch into the `master` branch.

### 6. Delete a Branch

#### Locally:

```sh
git branch -d <branch_name>
```

Deletes the branch locally.

#### Remotely:

```sh
git push origin --delete <branch_name>
```

Deletes the branch from the remote repository.

---

## 📂 Standard `.gitignore` Content

```sh
# Dependencies  
/node_modules  
/.pnp  
.pnp.*  
.yarn/*  
!.yarn/patches  
!.yarn/plugins  
!.yarn/releases  
!.yarn/versions  

# Testing  
/coverage  

# Next.js  
/.next/  
/out/  

# Production Builds  
/build  
/dist  

# Miscellaneous  
.DS_Store  
*.pem  

# Debugging Logs  
npm-debug.log*  
yarn-debug.log*  
yarn-error.log*  
.pnpm-debug.log*  

# Environment Variables (can opt-in for committing if needed)  
.env*  

# Vercel  
.vercel  

# TypeScript  
*.tsbuildinfo  
next-env.d.ts  

# Google Apps Script  
.clasp.json  

# React (if using service workers)  
/service-worker.js  
/precache-manifest.*.js  

# Generated IDE Settings (VS Code, JetBrains)  
.vscode/  
.idea/  
*.iml  

# Logs  
logs  
*.log  
yarn-debug.log*  
yarn-error.log*  
.pnpm-debug.log*  
```

