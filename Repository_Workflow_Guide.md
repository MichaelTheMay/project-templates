
# Workflow Guide for Managing the Repository

If you are the sole manager of this repository, you can streamline your workflow without needing to open pull requests (PRs). This guide provides clear steps for maintaining a clean and organized repository while minimizing redundant processes.

---

## Table of Contents
1. [Branching Strategy](#branching-strategy)
2. [Adding a New Template](#adding-a-new-template)
3. [Modifying an Existing Template](#modifying-an-existing-template)
4. [Testing and Validating Changes](#testing-and-validating-changes)
5. [Syncing with Remote Repository](#syncing-with-remote-repository)

---

## Branching Strategy

While PRs are not required, it’s still important to use branches to keep your work organized. Here's a recommended branching strategy:

1. **`main` (Stable Branch):**
   - Always contains stable, production-ready templates.
   - Changes are merged here only after testing.

2. **`develop` (Working Branch):**
   - Used for ongoing work and staging updates before merging to `main`.

3. **Feature Branches:**
   - Create a new branch for each new template or modification.
   - Naming conventions:
     - **New Template:** `feature/new-template-{name}`
     - **Modification:** `feature/update-template-{name}`
     - **Bug Fixes:** `fix/{description}`

---

## Adding a New Template

### Step 1: Create a New Branch
1. Switch to the `develop` branch:
   ```bash
   git checkout develop
   ```
2. Create a new branch for the template:
   ```bash
   git checkout -b feature/new-template-{name}
   ```

### Step 2: Add the Template
1. Create a new folder in the `templates` directory:
   ```bash
   mkdir templates/{template_name}
   ```
2. Add the template files and a `README.md` with instructions for use.

### Step 3: Commit Changes
1. Stage your files:
   ```bash
   git add .
   ```
2. Commit the changes:
   ```bash
   git commit -m "Add new template: {name}"
   ```

### Step 4: Merge to `develop`
1. Switch to the `develop` branch:
   ```bash
   git checkout develop
   ```
2. Merge the feature branch:
   ```bash
   git merge feature/new-template-{name}
   ```

---

## Modifying an Existing Template

### Step 1: Create a Branch
1. Switch to the `develop` branch:
   ```bash
   git checkout develop
   ```
2. Create a new branch for the modification:
   ```bash
   git checkout -b feature/update-template-{name}
   ```

### Step 2: Make Changes
- Edit the necessary files and update the `README.md` as needed.

### Step 3: Commit Changes
1. Stage the changes:
   ```bash
   git add .
   ```
2. Commit the changes:
   ```bash
   git commit -m "Update template: {name} - {brief description}"
   ```

### Step 4: Merge to `develop`
1. Switch to the `develop` branch:
   ```bash
   git checkout develop
   ```
2. Merge the feature branch:
   ```bash
   git merge feature/update-template-{name}
   ```

---

## Syncing with Remote Repository

Once your changes are merged into `develop` or `main`, push them to the remote repository.

### Step 1: Push `develop` Changes
```bash
git push origin develop
```

### Step 2: Merge `develop` into `main`
1. Switch to the `main` branch:
   ```bash
   git checkout main
   ```
2. Merge `develop` into `main`:
   ```bash
   git merge develop
   ```
3. Push `main` to the remote repository:
   ```bash
   git push origin main
   ```

---

## Best Practices

1. **Commit Often:** Make small, meaningful commits to make tracking changes easier.
2. **Document Everything:** Ensure each template has a clear `README.md`.
3. **Backup Regularly:** Push changes to the remote repository frequently to avoid data loss.

---

By following this guide, you can efficiently manage your repository without requiring a formal PR process. Happy coding! 🚀
