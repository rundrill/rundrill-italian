# RunDrill Italian

Your personal **Italian coach** inside your AI agent — short production-first drills, an honest
picture of your level (A1–C2), and mistake memory that resurfaces what you got wrong. The skill is
the voice; your level, weak topics, vocabulary, and goal live on the RunDrill MCP server
(`mcp.rundrill.com`), synced across machines — not in a local file.

The coach explains in your native language and moves toward Italian as your level rises
(comprehensible input, i+1), and drills what Italian actually turns on — double consonants (gemination), open vs closed vowels, essere vs avere, the congiuntivo, the particles ci and ne.

## One plugin, three hosts

The coaching skill (`skills/italian-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its
own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

On first use the host opens a browser tab for the OAuth handshake with `mcp.rundrill.com`, then
closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill languages marketplace:
  ```
  /plugin marketplace add rundrill/rundrill-lang
  /plugin install rundrill-italian@rundrill-lang
  ```
  Then run `/italian-coach`.
- **OpenAI Codex** — add the RunDrill languages catalog, then install `rundrill-italian`:
  ```
  codex plugin marketplace add rundrill/rundrill-lang
  ```
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-italian/` (global)
  or `<workspace>/.agents/plugins/rundrill-italian/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE).

In short, you **may** view, run, and share this plugin unchanged, for non-commercial purposes, **as
long as you give credit**. You **may not** use it commercially, or publish modified or derivative
versions (forks, ports, reworded skills).

Required attribution when sharing: *“RunDrill Italian coach — © RunDrill, CC BY-NC-ND 4.0,
https://rundrill.com”.*

For commercial use, derivatives, or any license beyond CC BY-NC-ND 4.0, contact
**hello@rundrill.com**.
