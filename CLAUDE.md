# illogical

## Pull requests

- Open PRs ready for review, never as drafts.
- After opening one, watch its CI. When a check fails, find the cause, fix it
  on the PR's branch and push; repeat until every check is green. Never
  skip, disable or weaken a test to get there.
- Once every check on the latest commit is green and the PR has no merge
  conflict, merge it: enable auto-merge, or merge it directly when the repo
  doesn't allow auto-merge. Use a merge commit, as the history does.
- Never merge a PR whose checks are red, still running, or never ran.
- A failure you can't fix from the PR: say what is failing and why, on the
  PR and to the user, and leave it open.

CI is `.github/workflows/check.yml` on GitHub's hosted runners: `linux`
(`just check` and the rest), and `macos` on Apple silicon and Intel
(`macos-15-intel`). Run what you can of it locally before pushing:
`just check`, `just test-scripts`.
