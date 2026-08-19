# Instalação rápida

SEFAZ MT: Consulta Credenciamentos é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_sefaz_mt_credenciamentos`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `SEFAZ MT: Consulta Credenciamentos` / `https://api.mcp.ai/p_sefaz_mt_credenciamentos`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "sefaz_mt_credenciamentos": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_mt_credenciamentos" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=sefaz_mt_credenciamentos&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZWZhel9tdF9jcmVkZW5jaWFtZW50b3MifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "sefaz_mt_credenciamentos": { "url": "https://api.mcp.ai/p_sefaz_mt_credenciamentos" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=sefaz_mt_credenciamentos&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_sefaz_mt_credenciamentos%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "sefaz_mt_credenciamentos": { "type": "http", "url": "https://api.mcp.ai/p_sefaz_mt_credenciamentos" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_sefaz_mt_credenciamentos
```

Dúvidas? [sefaz_mt_credenciamentos@mcp.ai](mailto:sefaz_mt_credenciamentos@mcp.ai)
