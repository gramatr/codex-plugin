# grāmatr Codex Plugin

> Real-time intelligent context engineering for OpenAI Codex, packaged as a Codex plugin marketplace repo.

## Install

Public mirror:

```
codex plugin marketplace add https://github.com/gramatr/codex-plugin
```

Private mirror or fork:

```
codex plugin marketplace add git@github.com:YOUR_ORG/YOUR_PRIVATE_CODEX_PLUGIN_REPO.git
```

Then open Codex, run `/plugins`, select `grāmatr Private`, open `grāmatr`, and choose `Install plugin`.

The current Codex manual documents GitHub shorthand, HTTPS Git URLs, SSH Git URLs, and local marketplace roots for `codex plugin marketplace add`, then documents installing from the Codex plugin browser.

Codex fetches the marketplace source, reads `.agents/plugins/marketplace.json`, installs `plugins/gramatr`, and connects the `gramatr` MCP server at `https://api.gramatr.com/mcp`. On first connection, sign in with the same identity you use at [gramatr.com](https://gramatr.com). No API key, no local npm package, no postinstall hook.

## What this gets you

Every prompt can be pre-classified and loaded with an intelligence contract — behavioral directives, quality criteria, and relevant context from past work — before the model responds.

- **System-prompt collapse** — a structured contract replaces the tens of thousands of tokens of behavioral enforcement you'd otherwise hand-maintain
- **Semantic retrieval** — past decisions, preferences, and project state pulled in automatically
- **Consistent behavior** — the same directives and quality gates on every prompt, every session, every tool; each output gated with recorded evidence

## What this repo is

This repository is the **public, reviewable source** for the grāmatr Codex plugin. It mirrors the files Codex reads at install time so a reviewer or user can audit the connector before installing.

- `.agents/plugins/marketplace.json` — Codex marketplace listing for the `gramatr` plugin
- `plugins/gramatr/.codex-plugin/plugin.json` — Codex plugin manifest
- `plugins/gramatr/.mcp.json` — MCP server registration for hosted grāmatr
- `LICENSE` — grāmatr License v1.0

The mirror is generated automatically from the [gramatr monorepo](https://github.com/gramatr/gramatr) release pipeline; do not open PRs against this repo directly.

## Learn more

- Product: <https://gramatr.com>
- Source (monorepo): <https://github.com/gramatr/gramatr>

## Version

0.32.12
