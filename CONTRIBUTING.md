# Contributing to Git Mentor

Thank you for contributing to Git Mentor!

## 1. Create a Feature Branch

Start from the latest `main` branch and create a separate branch for your work.

```bash
git switch main
git pull --ff-only origin main
git switch -c feature/short-description
```

Never develop features directly on the protected `main` branch.

## 2. Make and Review Your Changes

Keep changes focused on a single issue or feature.

Before staging, inspect your working tree:

```bash
git status
git diff
```

Stage the files you intend to commit:

```bash
git add <file>
git diff --staged
```

Review the staged changes before committing.

## 3. Write Meaningful Commits

Use descriptive commit messages that explain the change.

```bash
git commit -m "Add contributor guide"
```

Avoid vague messages such as `updates` or `fixed stuff`.

## 4. Push Your Feature Branch

Push the feature branch to GitHub:

```bash
git push -u origin feature/short-description
```

The `-u` option configures the upstream branch for future pushes.

## 5. Open a Pull Request

Open a Pull Request targeting `main`.

In the description:
- Explain what changed and why.
- Reference the relevant GitHub Issue.
- Describe the tests or checks performed.

Do not push feature changes directly to the protected `main` branch.

## 6. Pass Required Checks

Wait for the required GitHub Actions checks to complete.

Resolve any failed checks before merging. Required CI checks must pass before the Pull Request can be merged.

## 7. Merge and Clean Up

Once the Pull Request satisfies the repository's requirements, merge it through GitHub.

Update your local `main` branch:

```bash
git switch main
git pull --ff-only origin main
```

When the feature branch is no longer needed, delete it:

```bash
git branch -d feature/short-description
```

## 8. Security Guidelines

- Never commit passwords, API keys, tokens, or private keys.
- Keep commits focused and review changes before pushing.
- Follow the repository's branch protection and review requirements.

Thank you for helping improve Git Mentor!
