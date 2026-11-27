# .github

Account-level files for cesararroba, a personal GitHub account.

This repository must stay public. GitHub applies the default community health files below to every
repository of the account only when they come from a public `.github` repository.

| Path | What it does |
|---|---|
| `SECURITY.md` | Default security policy |
| `.github/ISSUE_TEMPLATE/` | Default issue forms: feature, task, bug; blank issues off |
| `.github/pull_request_template.md` | Default pull request template |
| `workflow-templates/` | Starter workflows to copy into a repo (user accounts do not get the Actions tab picker); they call the shared reusable workflows |
| `.github/workflows/reusable-*.yml` | Shared CI: actionlint, zizmor and site checks (pnpm scripts, optional Playwright) |

Repos call the reusable workflows here, pinned by commit SHA with the release tag as a comment
(`uses: cesararroba/.github/.github/workflows/reusable-zizmor.yml@<sha> # v1.0.0`). Tag a new
release after changing one, then bump the callers.

This is a user account, so there is no `profile/` directory here: the public profile lives in
[`cesararroba/cesararroba`](https://github.com/cesararroba/cesararroba).
