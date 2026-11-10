# Claude Code sandbox instructions

Before doing any task:
1. Read this CLAUDE.md and HANDOFF.md from the checked-out branch.
2. Read relevant workflow files and inspect current GitHub state; never assume HANDOFF is current without verification.
3. Report the current branch, main SHA, task scope, and any blockers in the task comment.
4. Only modify this sandbox repository unless the user explicitly authorizes a different repository in a separate task.

Execution:
- Use a task branch and propose changes through a pull request. Do not push directly to main.
- Never auto-merge, deploy, or alter production repositories.
- Do not access, display, collect, or store credentials, tokens, clipboard secrets, or private keys.
- Never claim success without checking command exit codes and resulting files/commits.
- If a task asks for a PR, create it when permitted. If unable, give a working compare link and explicitly report PR not created.
- Keep each PR focused; avoid mixing authentication experiments with documentation changes.
- Limit repeated identical failures to two; limit GPT/Claude review exchanges to three.
- Preserve existing workflows unless a change is explicitly needed and reviewed.
- Provide a final summary: changed files, commit SHA, PR URL/number, tests, and remaining work.

For authentication:
- The human performs `claude setup-token` and `gh secret set` interactively on PC03.
- Claude must never read or print the token. Check only the GitHub Secret name.
