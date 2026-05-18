<div align="center">

# OpenPlaybooks

**AI Agent harnessing for durable autonomous playbooks.**

[![npm version](https://img.shields.io/npm/v/@openplaybooks/converge?color=cb3837&logo=npm&label=npm)](https://www.npmjs.com/package/@openplaybooks/converge)
[![GitHub stars](https://img.shields.io/github/stars/openplaybooks-dev/converge?logo=github&color=181717)](https://github.com/openplaybooks-dev/converge/stargazers)
[![License: MIT](https://img.shields.io/github/license/openplaybooks-dev/converge?color=blue)](https://github.com/openplaybooks-dev/converge/blob/main/LICENSE)
[![Node](https://img.shields.io/node/v/@openplaybooks/converge?color=339933&logo=node.js&logoColor=white)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.7%2B-3178c6?logo=typescript)](https://www.typescriptlang.org/)

[Converge](https://github.com/openplaybooks-dev/converge) · [npm](https://www.npmjs.com/org/openplaybooks) · [Docs](https://github.com/openplaybooks-dev/converge/tree/main/docs) · [Examples](https://github.com/openplaybooks-dev/converge/tree/main/examples)

</div>

---

## What we build

The current AI agent landscape is powerful, but still fragmented and manual. We have good models, good tools, and good skills, but turning them into a reliable workflow for complex work still takes a lot of glue.

OpenPlaybooks builds the framework for **autonomous playbooks** — versioned, inspectable markdown artifacts that chain tasks and skills into a workflow an agent can run end to end, with checks, retries, and self-correction built into the loop.

**Not a static workflow. A living playbook.**

---

## Flagship project

### [Converge](https://github.com/openplaybooks-dev/converge)

A build system for AI agents. You write playbooks as markdown files and folders; Converge compiles them into a DAG and dispatches AI agents to run it. **Diverge → converge:** break a big problem into independent pieces, run them in parallel, assemble the result.

- **Checks, not vibes** — shell-command verification (`tsc`, `eslint`, tests). No LLM judging its own output.
- **Fingerprint caching** — SHA-256 per node. Kill at task 47; resume from what completed.
- **DAG, not context window** — each TASK.md fits in one window. The runtime chains them. 670 tasks, zero lost context.
- **Swap providers, not workflows** — Claude, Gemini, Kimi, Qwen, Codex behind one config.

---

## Packages

All packages are published under the [`@openplaybooks`](https://www.npmjs.com/org/openplaybooks) npm scope.

### Core

| Package | Purpose |
|---|---|
| [`@openplaybooks/converge`](https://www.npmjs.com/package/@openplaybooks/converge) | CLI for Converge — `converge init`, `converge add`, `converge run` |
| [`@openplaybooks/converge-core`](https://www.npmjs.com/package/@openplaybooks/converge-core) | Build system engine — plan, execute, verify, fix, ship |
| [`@openplaybooks/agentfn`](https://www.npmjs.com/package/@openplaybooks/agentfn) | Unified agent interface — switch between Claude, Kimi, Qwen, Gemini in one call |

### Provider adapters

| Package | Purpose |
|---|---|
| [`@openplaybooks/claudefn`](https://www.npmjs.com/package/@openplaybooks/claudefn) | Claude Code CLI as a function |
| [`@openplaybooks/codexfn`](https://www.npmjs.com/package/@openplaybooks/codexfn) | OpenAI Codex CLI as a function |
| [`@openplaybooks/geminifn`](https://www.npmjs.com/package/@openplaybooks/geminifn) | Gemini CLI as a function — with agentic loops |
| [`@openplaybooks/kimifn`](https://www.npmjs.com/package/@openplaybooks/kimifn) | Kimi CLI as a function — with agentic loops |
| [`@openplaybooks/qwenfn`](https://www.npmjs.com/package/@openplaybooks/qwenfn) | Qwen CLI as a function — with agentic loops |
| [`@openplaybooks/acpfn`](https://www.npmjs.com/package/@openplaybooks/acpfn) | Anthropic Client Protocol (Claude Agent SDK) as a function |
| [`@openplaybooks/openfn`](https://www.npmjs.com/package/@openplaybooks/openfn) | Opencode AI client as a function |
| [`@openplaybooks/deepcodefn`](https://www.npmjs.com/package/@openplaybooks/deepcodefn) | HKUDS DeepCode CLI as a function |

### Utilities & benchmarks

| Package | Purpose |
|---|---|
| [`@openplaybooks/codets`](https://www.npmjs.com/package/@openplaybooks/codets) | Fluent, indentation-aware source code emitter for TypeScript/JSX |
| [`@openplaybooks/converge-provider-benchmark`](https://www.npmjs.com/package/@openplaybooks/converge-provider-benchmark) | Deep journal analysis for comparing AI backends across playbook runs |
| [`@openplaybooks/converge-swebench`](https://www.npmjs.com/package/@openplaybooks/converge-swebench) | SWE-bench Lite runner for Converge |
| [`@openplaybooks/converge-tbench`](https://www.npmjs.com/package/@openplaybooks/converge-tbench) | Terminal-bench runner for Converge |

---

## Get started

```bash
# 1. Install
npm install -g @openplaybooks/converge

# 2. Bootstrap a project
converge init --name=my-project --provider-template=codex

# 3. Run a built-in example, or generate one from a prompt
converge add --from-example hello-world
converge run
```

The five-minute walkthrough: **[Your first playbook](https://github.com/openplaybooks-dev/converge/blob/main/docs/getting-started/your-first-playbook.md)**.

> ⚠️ Converge dispatches AI agents that call LLM APIs. A playbook can consume tens of millions of tokens — pick a cheap model in the provider config.

---

## Links

- **Source:** [github.com/openplaybooks-dev/converge](https://github.com/openplaybooks-dev/converge)
- **Issues:** [openplaybooks-dev/converge/issues](https://github.com/openplaybooks-dev/converge/issues)
- **Discussions:** [openplaybooks-dev/converge/discussions](https://github.com/openplaybooks-dev/converge/discussions)
- **npm:** [npmjs.com/org/openplaybooks](https://www.npmjs.com/org/openplaybooks)
- **Code of conduct:** [Contributor Covenant v2.1](https://github.com/openplaybooks-dev/converge/blob/main/CODE_OF_CONDUCT.md)
- **Security:** [report privately](https://github.com/openplaybooks-dev/converge/blob/main/SECURITY.md) via GitHub Security Advisories
- **Contact:** minh.lucvan@ncc.asia

---

<sub>MIT licensed. Copyright © 2026 Converge Framework Contributors.</sub>
