# AGENTS.md

Read by review agents that run against this repository from GitHub (the Codex review
workflow, per scout-dev-claude ADR 0001). The repo's `CLAUDE.md`, if present, is the
full set of conventions for people and their sessions; this is the subset a reviewer
needs.

## Code Review Rules

**Report only what you can point at.** Every finding names a file and a line, says
what breaks under which input, and cites the rule, test, doc or platform fact it rests
on. No praise, no summaries, no "consider" suggestions.

**Never propose the fix in code.** Name the defect and its source. The author chooses
the fix; that is how they learn it.

**Serious means one of these:**

- A wrong result, a crash, or lost data on a real input.
- A secret, credential, client name, or private path reaching the repository or a log.
- A break on a platform this repo supports. - A shell command that builds an argument list in a string, or silences stderr on a
  command whose failure matters.
- A claim of success that no command in the change actually verifies.
- Text a person will read that uses UK spelling, an em dash, or an AI-tell phrase
  (leverage, utilize, delve, robust, streamline). US English everywhere.

**Already covered, do not repeat:** **How your review is used.** Your findings are raw material. The author answers each
one on the PR, held or died with the evidence, and a human reviewer reads the diff
before reading you. You do not approve, and a PR never waits for you.
