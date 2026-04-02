# QA Handoff

Evidence-first QA gate for implementation work before final user handoff.

Use this skill after coding is finished and before reporting results. It defaults to a single QA reviewer and can switch to a stronger two-reviewer gate when you want both `qa-1` and `qa-2`. The protocol prefers runtime evidence over static inspection, treats ambiguous review output as `FAIL`, and stops after 3 failed rounds.

## Included

- `.agents/skills/qa-handoff/` - skill entrypoint and reference docs
- `.github/agents/` - GitHub Copilot agent definitions
- `.cursor/agents/` - Cursor agent definitions

## Install

Copy the skill into your agent harness's skill location:

```text
.agents/skills/qa-handoff/
```

If your environment resolves named agents from local files, also copy the matching agent definitions:

- GitHub Copilot: `.github/agents/qa.md`, `.github/agents/qa-1.md`, `.github/agents/qa-2.md`
- Cursor: `.cursor/agents/qa.md`, `.cursor/agents/qa-1.md`, `.cursor/agents/qa-2.md`

## Usage

- Use the default mode for a fast single-reviewer QA pass.
- Use two-QA mode when you want both reviewers to pass in the same round.
- Do not use this skill for planning-only work or mid-implementation checks.