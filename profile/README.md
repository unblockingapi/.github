<a href="https://unblockingapi.com">
  <img src="assets/hero.svg" alt="UnblockingAPI — One API call. Clean HTML back. A terminal shows GET /unblock returning 200 OK where a 403 used to be." width="100%">
</a>

**Send a public URL, get clean HTML back.** We handle browser rendering, country routing, retries and anti-bot handling — so you don't manage proxies, browser farms or credit calculators.

🌐 [unblockingapi.com](https://unblockingapi.com) · 📖 [API docs](https://unblockingapi.com/docs) · 💰 [Pricing](https://unblockingapi.com/pricing) · 🔒 [Security](https://unblockingapi.com/security) · ✉️ [hello@unblockingapi.com](mailto:hello@unblockingapi.com)

## Try it

Every account starts with **1,000 free requests** — no credit card. [Get your API key →](https://unblockingapi.com)

```bash
curl -H "X-Api-Key: YOUR_API_KEY" \
  "https://api.unblockingapi.com/unblock?url=https://example.com"
```

JavaScript-heavy page? Add `render=true` and it goes through a real stealth browser. Pick a country with `location`:

```bash
curl -H "X-Api-Key: YOUR_API_KEY" \
  "https://api.unblockingapi.com/unblock?url=https://example.com&render=true&location=se"
```

Every response has the same predictable shape:

```json
{
  "status": "succeeded",
  "http_response_code": 200,
  "response_time_ms": 1250,
  "location": "se",
  "response_format": "html",
  "response": "<!doctype html>..."
}
```

Or from code:

```js
const res = await fetch(
  "https://api.unblockingapi.com/unblock?url=https://example.com&render=true",
  { headers: { "X-Api-Key": process.env.UNBLOCKINGAPI_KEY } }
);
const { response: html } = await res.json();
```

More in the [API docs](https://unblockingapi.com/docs): POST requests, wait strategies for dynamic pages, structured template endpoints, and error codes.

## Using AI tools?

Give your agent the same superpower: `npx -y @unblockingapi/mcp` connects Claude, Cursor and any MCP client to the API — or grab [Unblocked](https://unblockingapi.com/tools), our free desktop app that renders blocked pages locally on your own IP.

## Elsewhere

[X](https://x.com/unblockingapi) · [Reddit](https://www.reddit.com/user/UnblockingAPI/) · [Product Hunt](https://www.producthunt.com/products/unblockingapi)

[![@unblockingapi/mcp MCP server – quality and maintenance score on Glama](https://glama.ai/mcp/servers/unblockingapi/mcp/badges/card.svg)](https://glama.ai/mcp/servers/unblockingapi/mcp)

[![@unblockingapi/mcp MCP server – quality and maintenance score on Glama](https://glama.ai/mcp/servers/unblockingapi/mcp/badges/score.svg)](https://glama.ai/mcp/servers/unblockingapi/mcp)
