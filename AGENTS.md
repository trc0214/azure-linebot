# Repository Agent Guidelines

## Scope and precedence

Apply instructions in this order:

1. User instructions for the current task.
2. This repository's `AGENTS.md` and more specific in-repo rules.
3. Governing workspace development rules, when available.
4. Tool defaults.

Do not invent project-specific commands or architecture assumptions. Read `README.md` and the relevant repository files before making implementation changes.

## Repository workflow

- GitHub is the canonical source for repository code, branches, commits, Issues, pull requests, checks, and implementation state.
- Keep `main` stable and do not perform feature development directly on it.
- Use one short-lived branch per task. AI branches use `ai/<agent>/<task>`.
- Keep pull requests focused and record applicable verification.
- Commits record history; Issues and pull requests record lifecycle state. Do not invent custom commit-state metadata.

## Issue AI attribution

- Every Issue must identify the human or AI agent/model that produced the initial Issue content.
- When the standard Bug/Implementation Issue Form is used, fill its required `Drafted By` field.
- If an Issue is created through Blank issue, GitHub CLI, API, or automation without the standard Issue Form, put `Drafted By: <human-or-agent/model>` at the top of the Issue body before creation. Do not create an Issue without initial attribution.
- Treat the initial `Drafted By` as immutable provenance; do not overwrite it during handoff, revision, or implementation.
- If another AI materially changes scope, acceptance criteria, reproduction, impact, dependencies, or other Issue-defining content, add one concise Issue comment beginning with `AI-Contributor: <agent/model>` and `Role: Planning`, `Role: Revision`, or `Role: Synthesis`. Routine wording edits do not require attribution.
- GitHub account identity records the operator account and must not be used to infer the actual AI contributor when explicit attribution exists.

## Handoff

If implementation ownership changes while the same task continues, leave concise durable context in the linked Issue or PR: previous and next owner, completed work, remaining work, verification, known risks, and next step.
