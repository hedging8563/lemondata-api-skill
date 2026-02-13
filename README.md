# LemonData API Integration Skill

<p align="center">
  <img src="https://lemondata.cc/logo.svg" alt="LemonData Logo" width="120">
</p>

<p align="center">
  <strong>Integrate 300+ AI APIs with any coding agent — Claude Code, Cursor, Copilot, Windsurf</strong>
</p>

<p align="center">
  <a href="https://lemondata.cc">Website</a> •
  <a href="https://docs.lemondata.cc/integrations/coding-agent-skill">Documentation</a> •
  <a href="https://lemondata.cc/en/models">Models</a> •
  <a href="https://lemondata.cc/#pricing">Pricing</a>
</p>

---

## What Can This Skill Do?

This skill teaches your coding agent how to integrate any of LemonData's AI APIs. The API is **Agent-First** — even if the agent guesses a model name wrong, the error response tells it exactly how to fix it.

1. **Try the API directly** — no searching needed
2. **Self-correct from errors** — structured hints like `did_you_mean` and `suggestions` guide the next attempt
3. **Generate complete, runnable code** in Python, JavaScript, Go, PHP, or cURL
4. **Pick the best model** based on real-time pricing and availability

## Installation

### npx (Recommended)

```bash
npx add-skill hedging8563/lemondata-api-skill -y
```

Installs to **all detected coding agents** automatically (Claude Code, Cursor, Copilot, etc.).

### Claude Code

```bash
# Personal (all projects)
git clone https://github.com/hedging8563/lemondata-api-skill.git ~/.claude/skills/lemondata-api-integration

# Project-specific (shared with team)
git clone https://github.com/hedging8563/lemondata-api-skill.git .claude/skills/lemondata-api-integration
```

### Verify

Ask your coding agent:
```
What skills are available?
```

## Quick Start

### Get Your API Key

1. Visit [lemondata.cc](https://lemondata.cc)
2. Go to [Dashboard → API Keys](https://lemondata.cc/dashboard/api)
3. Create and copy your key (`sk-...`)

### Start Using

Just describe what you need:

```
I want to use GPT-4 in my Python project
```

```
Generate images with Flux in Node.js
```

```
Integrate speech-to-text in my app
```

The agent will call the API, read any error hints, self-correct, and generate working code.

## Agent-First Error Recovery

Every error response includes structured hints:

| Error | API Returns | Agent Action |
|-------|------------|--------------|
| Wrong model name | `did_you_mean` + `suggestions` | Auto-corrects and retries |
| Insufficient balance | `balance_usd` + cheaper `suggestions` | Switches to affordable model |
| Model unavailable | `alternatives` + `retry_after` | Switches to available model |
| Rate limited | `retry_after` (exact seconds) | Waits and retries |
| Context too long | `suggestions` with larger models | Switches to bigger context model |

[Full Agent-First API reference →](https://docs.lemondata.cc/guides/agent-first-api)

## Supported Capabilities

| Type | Examples |
|------|----------|
| Chat | GPT-4o, Claude, Gemini, DeepSeek |
| Image Generation | Midjourney, Flux, Stable Diffusion |
| Video Generation | Sora, Runway, Kling, Luma AI |
| Music Generation | Suno |
| 3D Models | Tripo3D |
| Audio | Text-to-Speech, Speech-to-Text |
| Embeddings | text-embedding-3 |
| Rerank | bce-reranker, qwen3-rerank |

## Security

- ✅ Store API Key in environment variables
- ✅ Use backend frameworks for web apps
- ❌ Never expose API Key in frontend code
- ❌ Never commit API Key to Git

## Resources

- [Documentation](https://docs.lemondata.cc/integrations/coding-agent-skill)
- [Agent-First API](https://docs.lemondata.cc/guides/agent-first-api)
- [Available Models](https://lemondata.cc/en/models)
- [Pricing](https://lemondata.cc/#pricing)
- [Dashboard](https://lemondata.cc/dashboard)

## License

MIT License - see [LICENSE](LICENSE) for details.

---

<p align="center">
  Made with ❤️ by <a href="https://lemondata.cc">LemonData</a>
</p>
