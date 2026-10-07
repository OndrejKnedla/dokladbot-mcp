# DokladBot MCP server

Remote MCP server for [DokladBot](https://dokladbot.cz), Czech accounting for freelancers (OSVČ),
small companies and accounting offices. Connect your DokladBot account to Claude, ChatGPT,
VS Code, Cursor or any MCP client and ask about your documents, VAT and tax deadlines.

- **Endpoint:** `https://dokladbot.cz/api/mcp` (Streamable HTTP)
- **Auth:** OAuth 2.1 with dynamic client registration. The client opens the DokladBot sign-in page,
  you confirm access. You need a DokladBot account ([free trial](https://dokladbot.cz/registrace)).
- **Official MCP Registry:** `cz.dokladbot/dokladbot`
- **Docs:** [dokladbot.cz/funkce/ai-asistent](https://dokladbot.cz/funkce/ai-asistent)

## What you can ask

- Received and issued invoices, receipts, VAT breakdowns, overdue invoices
- VAT summary for a month or quarter, upcoming Czech tax deadlines
- Income and spending overview, bank transactions, suppliers
- Data box (datová schránka) messages
- Invoice drafts and receipt uploads, which always wait for your approval in the dashboard

The server never sends, deletes or pays anything on its own.

## Quick setup

**Claude (claude.ai, Desktop):** Settings, Connectors, Add custom connector, URL `https://dokladbot.cz/api/mcp`.

**VS Code / Cursor (`mcp.json`):**

```json
{
  "servers": {
    "dokladbot": { "type": "http", "url": "https://dokladbot.cz/api/mcp" }
  }
}
```

**Claude Code:**

```
claude mcp add --transport http dokladbot https://dokladbot.cz/api/mcp
```

---

## Česky

DokladBot shromáždí doklady na jednom místě: účtenky posíláte z mobilu přes WhatsApp, faktury
e-mailem a doklady z datové schránky se stáhnou samy. Účetní je jedním klikem převezme do Pohody,
Money S3 nebo ABRA Flexi. Přes tento MCP server se na svá data zeptáte přímo v AI asistentovi.

- [Všechny funkce](https://dokladbot.cz/funkce)
- [Ceník](https://dokladbot.cz/cenik)
- [Adresář účetních a daňových poradců](https://dokladbot.cz/ucetni)
- [Přehled úřadů: finanční úřady, OSSZ, zdravotní pojišťovny](https://dokladbot.cz/urady)
- [Blog o daních a účetnictví pro OSVČ](https://dokladbot.cz/blog)

Podpora: info@dokladbot.cz, [ochrana osobních údajů](https://dokladbot.cz/ochrana-osobnich-udaju).

This repository contains only documentation and the registry manifest. The server is operated by
Eucalypt 4 s.r.o., IČO 22103741.
