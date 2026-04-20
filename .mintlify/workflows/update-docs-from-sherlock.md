---
name: Update docs from Sherlock product changes
on:
  push:
    - repo: jamesnavinhill/sherlock
      branch: main
context:
  - repo: jamesnavinhill/sherlock
automerge: false
---

Review the latest user-facing changes in `jamesnavinhill/sherlock` and update this documentation repository to match the shipped product behavior.

Focus on changes that affect:

- product capabilities
- setup or provider configuration
- deployment or hosting guidance
- UI flows that users can see or follow
- naming, terminology, or navigation that appears in the public product docs

Work inside the existing docs information architecture first. Prefer updating current pages under `features/`, `configuration/`, `deployment/`, and `concepts/` before creating new pages.

Success criteria:

- Every meaningful user-facing product change in the latest Sherlock push is either documented here or intentionally skipped as out of scope.
- Updated docs match current shipped behavior rather than roadmap intent.
- New docs edits follow the existing Sherlock Mintlify tone, structure, and page patterns.

## Important

- Skip internal-only refactors, test-only changes, dependency bumps, and implementation details that do not affect end users.
- Do not mirror Sherlock's internal engineering docs from `docs/operations`, `docs/plans`, `docs/reports`, or `_legacy` into the public docs unless a concrete end-user behavior changed.
- If a change affects setup, prefer updating `quickstart.mdx`, `provider-setup.mdx`, or pages under `deployment/`.
- If a change affects a workspace surface, prefer updating the relevant page under `features/`.
- If no public documentation changes are needed, do not open a PR.
