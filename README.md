# phenates-skills

Personal collection of [Agent Skills](https://agentskills.io) (SKILL.md format) for working with an Obsidian vault and Markdown, usable across Hermes Agent, Claude Code / Claude Desktop, and claude.ai.

## Skills

| Skill | Description | Status |
|---|---|---|
| [`markdown-flavor`](skills/markdown-flavor) | House Markdown conventions plus Obsidian Flavored Markdown syntax (wikilinks, embeds, callouts, properties). Applies to any Markdown file, not just Obsidian notes. | Actively maintained |
| [`obsidian-vault`](skills/obsidian-vault) | Access and write to an Obsidian vault via MCP: tool mechanics, default save folder, vault organization, plugin-specific behavior. | Actively maintained |
| [`json-canvas`](skills/json-canvas) | Create and edit JSON Canvas (`.canvas`) files. | Vendored from Kepano, unmodified |
| [`obsidian-bases`](skills/obsidian-bases) | Create and edit Obsidian Bases (`.base`) files. | Vendored from Kepano, unmodified |
| [`obsidian-cli`](skills/obsidian-cli) | Obsidian CLI interaction. | Vendored from Kepano, not adopted (redundant with the Local REST API MCP server in use) |

## Install

### Hermes Agent

```bash
hermes skills tap add phenates/phenates-skills
hermes skills install phenates/phenates-skills/markdown-flavor
hermes skills install phenates/phenates-skills/obsidian-vault
hermes skills install phenates/phenates-skills/json-canvas
hermes skills install phenates/phenates-skills/obsidian-bases
```

Update with `hermes skills update` (or `hermes skills check` to preview).

### Claude Code / Claude Desktop (Code tab)

Via the `npx skills` CLI (symlinked, single source of truth):

```bash
npx skills add https://github.com/phenates/phenates-skills -a claude-code -g
```

Or via the Claude Code plugin marketplace:

```
/plugin marketplace add phenates/phenates-skills
/plugin install phenates-skills@phenates-skills
```

### claude.ai / Claude Desktop (Chat)

No filesystem or Git access on this surface. Zip each skill folder (`SKILL.md` plus its `references/` folder, if any) and upload individually via Settings > Capabilities > Skills.

## License

This repository's own content (`markdown-flavor`, `obsidian-vault`) is MIT licensed -- see [LICENSE](LICENSE).

`json-canvas`, `obsidian-bases`, and `obsidian-cli` are vendored unmodified from [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills), MIT licensed by kepano.
