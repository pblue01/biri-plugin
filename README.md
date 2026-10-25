# BIRI&trade; for Claude

Ground Claude's answers in BIRI&trade;'s curated, human-rated reference
library. When you ask a substantive question, Claude extracts the key terms,
searches BIRI&trade; for curated references, reads the top sources, and gives
you an answer that cites each one with its curator rating. If the archive has
nothing curated on the subject, Claude says so instead of answering from
memory.

Works in Claude.ai chat, Cowork, and Claude Code.

## What's included

| Component | What it does |
| --- | --- |
| `biri` connector (remote MCP server at `https://mcp.planetary.blue/mcp`) | Tools to search the BIRI&trade; archive, check your remaining consultations, look up your profile, list categories, and suggest a reference for curation |
| `biri-search` skill | Tells Claude when to consult BIRI&trade; — substantive factual, research, and how-to questions, not small talk or code-only tasks |

## Setup

1. Add the plugin from the Claude directory, or in Claude Code run:

   ```
   /plugin install biri --marketplace pblue01/biri-plugin
   ```

2. Open the plugin's **Connectors** tab and select **Connect** (in Claude
   Code, run `/mcp` and choose `biri`).
3. Sign in to your BIRI&trade; account and approve the request.

There is no API key to create or paste.

## Credits

Each archive search uses one of your BIRI&trade; search credits. Your monthly
allowance depends on your BIRI&trade; membership tier; some tiers are
unlimited. When your credits for the period are used up, Claude tells you when
they renew and where to upgrade. Ask Claude "how many BIRI consultations do I
have left?" at any time.

## Data and privacy

- **What is sent:** the search keywords Claude extracts from your question,
  any URL you ask Claude to suggest for curation, and your BIRI&trade; access
  token.
- **Where it goes:** to the BIRI&trade; MCP server at `mcp.planetary.blue`,
  which forwards it to the BIRI&trade; backend at `biribckd.planetary.blue`.
  The MCP server does not store your token or your queries.
- **What is kept:** the BIRI&trade; backend logs each search against your
  account to count credits.
- **What else happens:** Claude fetches the public web pages of the
  references BIRI&trade; returns, using its own web-fetch tool.

Nothing is sent to any other service. You can disconnect the connector at any
time, and revoking your access in your BIRI&trade; account takes effect on the
next request.

## Support

Contact adminx@planetary.blue.

## License

MIT — see [LICENSE](LICENSE).
