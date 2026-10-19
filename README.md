# COMP1117 T5 Playground

# features

A **practice repository** for the COMP1117 Tutorial 5 (Advanced GitHub: branching, pushing, pulling, merging).
Nothing here matters - break it, fix it, learn from it.

## Quick start

```bash
git clone https://github.com/Mohit-pjcts/comp1117-t5-playground.git
cd comp1117-t5-playground
git switch -c feature/<your-name>          # 1. create your own branch
# add a file students/<your-name>.txt       # 2. edit
git add students/<your-name>.txt           # 3. stage
git commit -m "Add <your-name> to the roster"   # 4. commit
git push -u origin feature/<your-name>     # 5. publish the branch
```

Then open a **Pull Request** on GitHub (base `main` <- compare `feature/<your-name>`).

## What is in here

| Path                     | Used for                                                                 |
| ------------------------ | ------------------------------------------------------------------------ |
| `hello.py`               | a tiny script to edit on your branch                                     |
| `students/`              | add one file per person (no conflicts: everyone adds a _different_ file) |
| `conflict-lab/motto.txt` | the **merge conflict** exercise (see below)                              |

## Merge conflict exercise

Two ready-made branches change the **same line** of `conflict-lab/motto.txt` differently:

```bash
git fetch origin
git switch demo/conflict-a
git merge origin/demo/conflict-b       # CONFLICT - resolve it in VS Code, then commit
```

To redo it, `git merge --abort` (before you commit) or delete your local copy of the branch and fetch again.

## Ground rules

- Work on **your own branch**, never directly on `main`.
- `git pull` before you start and before you push.
- Do not delete other people's branches.
