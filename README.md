# agents-flow

Three planning steps for the Workflow of [agents-repo-setup](https://github.com/gianmadd/agents-repo-setup), between the spec and the code. They sit on top of [mattpocock/skills](https://github.com/mattpocock/skills): install those first.

| Skill | When | What it adds |
|---|---|---|
| `product-review` | after `/to-spec`, when the feature touches UI | an HTML mockup with success criteria per persona and edge case, in `.scratch/` |
| `system-architecture` | after `/to-spec`, unless it is a bug fix or a trivial feature | diagrams, contracts and domain invariants, appended to the spec |
| `program-design` | after `/to-tickets`, unless no signature changes | call tree, file changes and signatures, appended to each ticket |

`/implement-spec` then builds the tickets: its subagents read the spec and tickets, these sections included.

The skills hold no rules on git, accounts or trackers: those come from the repo's `AGENTS.md`, which the setup writes.

## Install

The setup installs them per repo. By hand:

```sh
npx skills add gianmadd/agents-flow -y
```

## Origin

Copied from [salvatorebottiglieri/agentic-dev-kit](https://github.com/salvatorebottiglieri/agentic-dev-kit) (MIT), with `CONTEXT.md` read as `GLOSSARY.md` and `implement-loop` replaced by `implement-spec`. Upstream changes are not merged in.
