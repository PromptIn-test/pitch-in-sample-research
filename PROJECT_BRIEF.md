# Project brief: pitch-in-sample-research

> Sample data, written to the Pitch In project-brief template.

## What the project does

Short research notes for an invented small business, written in Markdown. It is a throwaway repo for testing Pitch In with research work: each task produces one note that answers one question, with sources. It has no readers.

## Stack and versions

- Markdown only, no build step.
- CI runs markdownlint (markdownlint-cli2) on every `.md` file. Line length isn't checked (see `.markdownlint-cli2.jsonc`).

## Setup and test commands

```sh
npx markdownlint-cli2 "**/*.md"
```

That's the same lint CI runs. There's nothing else to install or run.

## Repo map

- `research/README.md`: the format every note follows, and how to cite sources
- `research/*.md`: one note per question
- `.github/workflows/docs-check.yml`: CI, runs markdownlint
- `.markdownlint-cli2.jsonc`: lint settings

## Conventions

- One note per question, named after the topic in kebab-case, e.g. `research/uptime-monitoring.md`.
- Each note has: a one-paragraph answer first, then a comparison table, then a short recommendation, then a numbered source list.
- Every claim in a table cites a source by number, e.g. `[2]`. Sources are public web pages with the date they were read.
- Plain language, short sentences, no marketing words.
- Commits: one short imperative line.

## Definition of done

- markdownlint passes.
- The note follows the format in `research/README.md`.
- Every claim in the table has a linked source; nothing is made up.
