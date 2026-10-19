# proteus-ai-experiments

Experiments connecting LLMs and agents to Proteus (github.com/ichellin1/proteus). The repo is
public, for learning and for showing in job interviews. Nothing here is released.

## How we work

- The goal is the journey: the user learns by reviewing what Claude did and asking questions.
  Keep each change small enough to review, and explain what it does and why.
- Lighter process than Proteus: no changelog and no release process.
- Commits use conventional commits, `type(scope): subject`, with the experiment's folder as the
  scope.
- Commit only when the user asks.

## Layout

- One folder per experiment at the repo root. Experiments that share code share it through the
  workspace, not by copying.
- A Cargo workspace for the Rust parts and an npm workspace for the TypeScript parts, added with
  the first experiment that needs each.

## Proteus

- Depend on Proteus's published releases (`proteus-sdk` on crates.io and npm).
- A local change to Proteus is the exception, not normal practice: only for a feature that will
  go into a Proteus release, and recorded as one in the Proteus repo. The user works on Proteus
  releases and these experiments in parallel.
- A gap in Proteus's public API that an experiment runs into is worth recording in the Proteus
  repo: it's feedback on what outside developers need.

## Demos

- Shown by recordings, the code, or a screen share. No hosted demo, so no API key ever reaches a
  browser or a server we run.
- API keys live in `.env`, which is gitignored. `.env.example` holds placeholder values.
