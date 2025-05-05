# Git Version Control Basics

This project explores the fundamentals of Git version control, focusing on branching, merging, and pull requests (PRs) in collaborative development environments. It includes practical examples of real-world Git workflows to help developers and teams manage their source code efficiently.

### Features
- Understanding Git repositories and version control principles
- Creating and managing branches
- Working with Pull Requests (PRs) for code collaboration
- Merging changes and resolving conflicts
- Context-based Git workflows for teams and open-source projects

### Installation
Ensure Git is installed on your system. You can verify installation by running:

```sh
git --version
```

If Git is not installed, download it from [git-scm.com](https://git-scm.com/) and follow the installation instructions.

### Git Workflow Examples

#### Initializing a Repository
Create a new Git repository:
```sh
git init my_project
cd my_project
```


### Creating and Switching Branches
Use branches to work on separate features:

```sh
git branch feature-branch
git checkout feature-branch
```

Or:

```sh
git switch -c feature-branch
```

#### Making and Committing Changes
After modifying files, commit changes:
```sh
git add .
git commit -m "Added new feature"
```

#### Creating a Pull Request (PR)
A Pull Request (PR) is used to propose changes before merging into the main branch.
1. Push the feature branch to a remote repository:

```sh
git push origin feature-branch
```

2. Go to GitHub/GitLab and create a Pull Request from `feature-branch` into `main`.
3. Team members review the PR, suggest changes, and approve the merge.

#### Merging Changes
After PR approval, merge the changes:

```sh
git checkout main
git merge feature-branch
```

Alternatively, merging via GitHub:
- Navigate to the PR page and click "Merge Pull Request".

#### Handling Merge Conflicts
If conflicts arise during merging, resolve them manually:
1. Open the conflicting files.
2. Edit and remove conflict markers (`<<<<<<<`, `>>>>>>>`).
3. Add the resolved file and commit:

```sh
git add resolved_file.txt
git commit -m "Resolved merge conflict"
```

#### Fetching & Pulling Changes
Sync local and remote repositories:

```sh
git fetch origin
git pull origin main
```

### Context-Based Workflows
#### Collaborative Team Workflow
- Developers create branches for individual features.
- PRs are submitted for review and merged into the main branch after approval.
- Conflicts are resolved collaboratively before merging.
