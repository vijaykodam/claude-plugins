# claude-plugins

The `vijaykodam` Claude Code plugin marketplace — a catalog repo that lists my
plugins. The plugin code lives in each plugin's own repository; this repo only
contains the marketplace manifest.

## Install

Add the marketplace once, then install any plugin from it:

```
/plugin marketplace add vijaykodam/claude-plugins
/plugin install url-logger@vijaykodam
/plugin install model-audit@vijaykodam
```

Or from your shell, outside a session:

```bash
claude plugin marketplace add vijaykodam/claude-plugins
claude plugin install url-logger@vijaykodam
claude plugin install model-audit@vijaykodam
```

Run `/reload-plugins` (or restart Claude Code) to activate newly installed
plugins. To pick up newly listed plugins later: `/plugin marketplace update vijaykodam`.

## Plugins

| Plugin | What it does | Repository |
|---|---|---|
| url-logger | Logs all WebSearch and WebFetch URLs to `.claude/web-access.log` with session IDs and timestamps | https://github.com/vijaykodam/url-logger |
| model-audit | Audits which Claude model handled each Claude Code session, from transcript ground truth; adds the `/model-audit:model-audit` command | https://github.com/vijaykodam/model-audit |

## Note for existing url-logger users

The url-logger repo ships its own marketplace manifest, also named
`vijaykodam`. Claude Code registers one marketplace per name, so adding this
repo replaces that entry — nothing breaks, and you gain the full catalog.
