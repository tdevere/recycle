Resolving Conflicts During a Pull Request
Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://.
```

Fetch the Latest Changes

Retrieve the latest changes from both the source and target branches:

```bash
git fetch origin
```

Create a New Branch

Create a new branch from the target branch to test the merge or cherry-pick:

```bash
git checkout -b test-merge origin/target-branch
```

Attempt to Merge

Try to merge the source branch into the new branch:

```bash
git merge origin/source-branch
```

Git will notify you if there are conflicts.

Identify Conflicting Files

List the files that have conflicts:

```bash
git status
```

Inspect Conflicts

Open each conflicting file to review the conflicts. They will be marked with sections like:

```plaintext
<<<<<<< HEAD
// Code from the target branch
// Code from the source branch

source-branch
```

Understand the Changes

Review the changes made in the conflicting areas using:

```bash
git log origin/source-branch -p <file-path>
```

and

```bash
git log origin/target-branch -p <file-path>
```

Resolve Conflicts

Decide how to resolve each conflict. Options include choosing one version, combining changes, or modifying the code. After resolving, save the file and close your editor.

Mark Conflicts as Resolved

Add the resolved files to the current commit:

```bash
git add <file-path>
```

Complete the Merge

Finish the merge process by committing:

```bash
git commit
```

