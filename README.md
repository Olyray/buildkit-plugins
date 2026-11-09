# buildkit

A Claude Code plugin with skills for planning and building apps.

## Skills

| Command | What it does |
|---|---|
| `/buildkit:ideate` | Explore ideas, tools, and approaches for an app or feature **before** you build anything. It asks you questions first, then lays out options with trade-offs. It does not write code. |

## Install

You need [Claude Code](https://code.claude.com) installed.

**One command (from your terminal):**

```bash
claude plugin install buildkit --marketplace Olyray/buildkit-plugins
```

Inside a Claude Code session, the same thing is:

```
/plugin install buildkit --marketplace Olyray/buildkit-plugins
```

**Or in two steps** (add the catalog first, then install from it):

```bash
claude plugin marketplace add Olyray/buildkit-plugins
claude plugin install buildkit@buildkit-plugins --scope user
```

Inside a session: `/plugin marketplace add Olyray/buildkit-plugins`, then `/plugin install buildkit@buildkit-plugins`.

If the command doesn't show up right away, run `/reload-plugins` or restart Claude Code.

## Use

Type the command and describe what you want to build:

```
/buildkit:ideate I want to add real-time notifications to my app
```

Claude will ask a few questions about your goals and constraints, then suggest several approaches and compare them. Claude may also pick the skill up on its own when you say things like "help me think through" or "what should I use for".

## Update

```bash
claude plugin marketplace update buildkit-plugins
claude plugin update buildkit@buildkit-plugins
```

## Uninstall

```bash
claude plugin uninstall buildkit@buildkit-plugins
claude plugin marketplace remove buildkit-plugins
```

## Layout

```
.claude-plugin/marketplace.json     the catalog (what `marketplace add` reads)
plugins/buildkit/
├── .claude-plugin/plugin.json      the plugin's details
└── skills/ideate/SKILL.md          the skill itself
```
