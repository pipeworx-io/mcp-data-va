# mcp-data-va

Virginia Open Data (datahub.va.gov) Socrata MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1000+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `datasets` | Search the Virginia Open Data catalog of open datasets by keyword. Returns each dataset\'s resource_id, name, description, category and update date — pass the resource_id to query/metadata. |
| `query` | Run a Socrata SoQL query against a Virginia Open Data dataset by resource_id (e.g. "rdpw-mtbs"). Filter with where/select/group/order (SoQL clauses, without the leading $) plus limit/offset. Returns matching rows as JSON. |
| `metadata` | Get a Virginia Open Data dataset\'s schema + metadata (columns, types, row count, category, last-updated) by resource_id, e.g. "rdpw-mtbs". |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-va": {
      "url": "https://gateway.pipeworx.io/data-va/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1000+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Va data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [All tools and guides](https://github.com/pipeworx-io/examples)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
