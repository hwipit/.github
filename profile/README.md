<h1 align="center">Your agent asks. You hwip it.</h1>

<p align="center">
  Coding agents stop when they need you. Hwip sends the question to your phone, with the diff,<br>
  and types your answer back into the same tmux session.
</p>

<p align="center">
  <a href="https://apps.apple.com/app/id6818053606">App Store</a> ·
  <a href="https://hwip.app">hwip.app</a> ·
  <a href="https://docs.hwip.app">Docs</a> ·
  <a href="https://hwip.app/security">What the server sees</a>
</p>

<p align="center">
  <img src="./demo.gif" alt="An agent asks 'Run the migration?' on the phone with the diff attached; you tap Run and the session keeps going" width="640">
</p>

## Get started

1. Install [Hwip on your iPhone](https://apps.apple.com/app/id6818053606) and sign in.
2. On your computer:
   ```bash
   npm install -g @hwip/cli && hwip install
   ```
3. Start your agent through Hwip: `hwip cc`, `hwip codex`, `hwip pi`, …

Using Claude Code? The plugin bundles the hooks, MCP server and rules:

```bash
claude plugin marketplace add hwipit/plugin
claude plugin install hwip@hwip
```

## Why Hwip

- **Sealed before it leaves your machine.** Questions and answers are encrypted with AES-256-GCM and a key per device, on the free plan too. [What the server still sees →](https://hwip.app/security)
- **The diff comes with the question.** Each question carries the session's `git diff` and its last terminal lines, secrets masked, so you can decide from the lock screen.
- **Not tied to one vendor.** Claude Code, Codex, pi, OpenCode, Gemini CLI and more in one list, with the same buttons. `hwip install` wires up 10 agents and the phone can type into 16.

## Repositories

| Repo | What it is |
|------|------------|
| [**plugin**](https://github.com/hwipit/plugin) | Claude Code plugin: hooks, MCP server and rules in one install |
| [**cli**](https://github.com/hwipit/cli) | `@hwip/cli`: push SDK, `hwip` command and the listener that lets your phone drive tmux sessions |
| [**mcp-server**](https://github.com/hwipit/mcp-server) | `@hwip/mcp-server`: `hwip_ask`, notifications, clipboard and files for any MCP client |

All three are Apache-2.0. Questions or bugs: open an issue in the repo, or write to support@hwip.app.
