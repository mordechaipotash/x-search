# x-search

**Search X/Twitter from your terminal. No Twitter API key needed.**

https://github.com/mordechaipotash/x-search/raw/main/assets/demo.mp4

---

## Install

```bash
curl -o ~/bin/x-search https://raw.githubusercontent.com/mordechaipotash/x-search/main/x-search
chmod +x ~/bin/x-search
export OPENROUTER_API_KEY="your-key"
```

## Use

```bash
x-search "mass layoffs tech 2026"
```

```
1. @kateclark · Feb 14, 2026
   "Stripe just laid off another 300 people..."
   🔗 https://x.com/i/status/1890421837492
   ❤️ 4.2K  🔁 1.8K  👁 890K

2. @pacaborern · Feb 14, 2026
   "Difficult decisions. Restructuring to focus on AI-native payments..."
   🔗 https://x.com/i/status/1890418293741
   ❤️ 12K  🔁 3.1K  👁 2.4M

💰 Cost: $0.006 | 🤖 grok-4.1-fast:online
```

---

## Why This Exists

| | Twitter API | x-search |
|---|---|---|
| Cost | $100/month minimum | ~$0.006/search |
| Auth | OAuth, approval process | One API key |
| Setup | 200+ lines Python | 0 lines (it's a script) |
| Rate limits | Yes | No |
| Real-time | Delayed | Live |

Twitter's API costs $100/month for basic search. Grok models on OpenRouter have native X search built in. This script wraps that.

---

## Options

```bash
x-search "topic"                              # Basic search
x-search "topic" --from 2026-02-01            # Date range
x-search "topic" --handles @elonmusk,@sama    # Filter by handle
x-search "topic" --raw                        # JSON output
x-search "topic" --model x-ai/grok-4:online   # Bigger model
```

## Dependencies

`curl` and `jq`. That's it. 151 lines of bash.

---

## Part of the ecosystem

[brain-mcp](https://github.com/mordechaipotash/brain-mcp) · [local-voice-ai](https://github.com/mordechaipotash/local-voice-ai) · [agent-memory-loop](https://github.com/mordechaipotash/agent-memory-loop) · [mordenews](https://github.com/mordechaipotash/mordenews)

## License

MIT
