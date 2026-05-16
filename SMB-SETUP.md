# LibreChat SMB Edition — Setup Guide

> Maintained by **Nataliya Brovkina** — Claude Implementation Specialist for small businesses.
> Site: [nataliyabrovkina.com](https://nataliyabrovkina.com) | Free audit: [Find your AI bottleneck](https://nataliyabrovkina.com/tools/bottleneck-calculator.html)

---

## What this is

This fork of LibreChat is configured specifically for small business AI implementation.
It includes ready-to-use MCP server connections, Claude workflow templates, and a setup
guide for legal, finance, ops, and marketing teams.

LibreChat gives you a self-hosted Claude interface with full MCP support — so your team
can use AI without sending data to third-party platforms.

---

## Who this is for

- Solo operators and small teams (1–50 people)
- Legal, compliance, and consulting firms
- Accounting and CFO offices
- Operations, services, and retail businesses
- Marketing and creative agencies

---

## Quick Start (SMB Edition)

### 1. Clone and install

```bash
git clone https://github.com/nibrovkina-cyber/LibreChat.git
cd LibreChat
cp .env.example .env
```

### 2. Add your Claude API key

```env
ANTHROPIC_API_KEY=your_key_here
```

Get a key at: https://console.anthropic.com

### 3. Connect MCP servers

Edit `librechat.yaml` to add MCP servers for your workflow:

```yaml
mcpServers:
  notion:
    type: stdio
    command: npx
    args: ["-y", "@notionhq/notion-mcp-server"]
  airtable:
    type: stdio
    command: npx
    args: ["-y", "airtable-mcp-server"]
```

### 4. Start

```bash
docker compose up -d
```

Access at: http://localhost:3080

---

## SMB Workflow Templates

Pre-built Claude prompts for common small business workflows:

| Workflow | Time saved | Setup time |
|----------|-----------|------------|
| Contract review and extraction | 8-12h/week | 3 days |
| Financial reporting automation | 10-15h/week | 2 days |
| Operations status summaries | 6-10h/week | 2 days |
| Marketing content production | 8-12h/week | 3 days |

Full workflow templates: [nataliyabrovkina.com](https://nataliyabrovkina.com)

---

## Not sure where to start?

Take the free **AI Bottleneck Calculator** — 10 questions, get a personalized
Claude Workflow Map showing exactly which process to automate first.

[Find my bottleneck](https://nataliyabrovkina.com/tools/bottleneck-calculator.html)

---

## Support

Built and maintained by Nataliya Brovkina.
Questions about implementation: [nataliyabrovkina.com](https://nataliyabrovkina.com)

Original LibreChat project: [github.com/danny-avila/LibreChat](https://github.com/danny-avila/LibreChat)
