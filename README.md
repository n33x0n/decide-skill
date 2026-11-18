# decide

An agent skill for reviewing what came back after a release. It makes the agent cite raw signals, recompute the owner's own metric, separate the size of an error from its reach and age, and say which calls belong to the owner.

## What it does

- Reads the signed decision record first: target, guardrails, window and who signed.
- Opens each source (text, audio, video) and cites file, line or second. Observations stay apart from claims and compliments.
- Recomputes the owner's metric, including state at a cutoff with reopen events.
- Groups findings by the underlying problem and gives each one a single verb: expand, revise, simplify, revert, investigate or stop.
- Separates bugs the agent may fix from product decisions that wait for the owner.

## Install

Copy the `decide/` folder into your agent's skills directory (for example `.omp/skills/`, `.claude/skills/` or `.agents/skills/`). The agent loads `SKILL.md`, which tells it to read `RULES.md` first.

## What breaks or doesn't work

It is written from one accepted review and tested on few cases. It does not fetch data, schedule anything or change a release. Video and audio work needs your agent to have tools for them.

## Files

- `decide/SKILL.md` — the routine.
- `decide/RULES.md` — the kept rule and its boundaries.

## License

Apache License 2.0, as the repository it was taken from.
