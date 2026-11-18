# DevRaftel plugins

Plugins that connect AI assistants to DevRaftel products.

## DevRaftel Recon

Recon prepares bank and card reconciliations for bookkeepers and small
accounting firms. You give it a client's bank statement and ledger. It matches
the lines, explains the ones it could not match, and returns an Excel
workpaper and a PDF summary. An accountant reviews and signs off. Recon never
posts or approves entries.

- Website: https://recon.devraftel.com
- Support: https://recon.devraftel.com/support
- Privacy: https://recon.devraftel.com/privacy
- Terms: https://recon.devraftel.com/terms

You need a DevRaftel account. Sign-in uses OAuth at `auth.devraftel.com`.
These plugins hold no credentials.

### Claude Code

```bash
claude plugin marketplace add devraftel/plugins
claude plugin install devraftel-reconciliation@devraftel
```

Then run `/mcp`, choose `devraftel-reconciliation` and sign in.

### Claude (web, desktop, mobile)

Add the connector in Settings → Connectors → Add custom connector with this
URL, then sign in:

```
https://api.finance.devraftel.com/mcp/reconciliation
```

### ChatGPT and Codex

The package for OpenAI's plugin directory is in
[`openai/devraftel-reconciliation`](openai/devraftel-reconciliation).

## Layout

| Path | What it is |
|---|---|
| `.claude-plugin/marketplace.json` | Claude marketplace `devraftel` |
| `devraftel-reconciliation/` | Claude plugin: MCP connector and workflow skill |
| `openai/devraftel-reconciliation/` | OpenAI plugin: `plugin.json`, `mcp.json`, skill, icons |
