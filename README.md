# NeurLead AI CRM — MCP server

<img src="assets/logo-512.png" alt="NeurLead" width="96">

Run your home-service CRM from your AI assistant: see who is waiting for a reply, draft replies and estimates from your own price list, check the schedule and unpaid invoices.

**Remote MCP endpoint (streamable HTTP, OAuth 2.0 with PKCE and dynamic client registration):** `https://mcp.neurlead.com/connect/mcp`

NeurLead is a CRM and AI dispatcher for home-service companies: handyman, cleaning, windows and glass, roofing, plumbing, painting and similar trades. Connect your own NeurLead workspace and your assistant works with your real data: leads and their chats, calls, your price list, schedule, technicians, estimates and invoices.

## What you can ask
- "Who is waiting for a reply, and what should I answer?"
- "Which invoices have been unpaid for more than three days?"
- "Which technicians are free Friday morning?"
- "Set up my CRM from our website and ask me only what is missing."

## You stay in control
- You sign in to your own workspace as its owner; the AI reaches that workspace only.
- For each area you choose whether the AI has no access, can look, or can change.
- Messages to customers start in "suggest only" mode: the AI drafts, a person sends.
- Recording an outside payment, voiding invoices or estimates, booking visits, starting a campaign, and changing prices or setup after go-live always wait for a person.
- Sensitive topics (refunds, cancellations, complaints, damage, contracts, card numbers) always go to a person.
- Every request is written to an audit log in your workspace; you can disconnect the AI at any moment.

## Connect
Claude: Settings → Connectors → Add custom connector → `https://mcp.neurlead.com/connect/mcp`

ChatGPT: add a custom MCP server with the same address.

Claude Code (plugin):

```
/plugin marketplace add Neurlead/neurlead-crm-mcp
/plugin install neurlead-crm@neurlead-crm
```

Gemini CLI (extension):

```
gemini extensions install https://github.com/Neurlead/neurlead-crm-mcp
```

Any MCP client:

```json
{ "mcpServers": { "neurlead-crm": { "type": "http", "url": "https://mcp.neurlead.com/connect/mcp" } } }
```

You need a NeurLead workspace: https://neurlead.com/signup

## Links
- Product: https://neurlead.com/connect
- Documentation: https://neurlead.com/connect/docs
- Privacy: https://neurlead.com/connect/privacy
- Terms: https://neurlead.com/connect/terms
- Official MCP Registry: `com.neurlead/crm`
- Contact: hello@neurlead.com
