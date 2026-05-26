# Cloud Platform - Advanced Git & DevOps Lab

## Lab 2: Rebase, Hotfixes, Stashing & Release Workflow

### Setup
- Repository: `cloud-platform`
- Initial file: `app.txt` (v1)

### Part 1 - Feature Development
- Branch: `feature/monitoring`
- Added CPU, memory, disk monitoring (3 commits)

### Part 2 - Hotfix
- Branch: `hotfix/security-patch`
- Applied security patch, merged to `main`
- Tagged: `v1.1`

### Part 3 - Rebase
- Rebased `feature/monitoring` onto `main`
- Resolved conflict in `app.txt`
- Result: Linear commit history

### Part 4 - Stashing
- Stashed incomplete monitoring alerts
- Switched branches safely
- Restored with `git stash pop`

### Part 5 - Multiple Remotes
- Added `origin` (GitHub) and `backup` (GitLab)
- Pushed to both remotes

### Part 6 - Release Tagging
- Merged `feature/monitoring` → `main`
- Tags: `v1.1` (hotfix), `v2.0` (full release)
- Pushed tags with `--tags`

### Part 7 - Undo Mistake
- Simulated broken config commit
- Recovered with `git revert`

### Key Commands
```bash
git rebase main
git stash push -m "message"
git stash pop
git remote add origin <url>
git remote add backup <url>
git tag -a v2.0 -m "message"
git revert HEAD
