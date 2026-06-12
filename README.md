# AI Content Pipeline

**A 5-agent n8n + Claude workflow that turns trending data into a camera-ready script — delivered to your inbox every week, fully automatically.**

---

## Why this exists

Content creation has three jobs hiding inside it: research, writing, and performing. Most creators are strong at performing and spend disproportionate time on the other two — scrolling for inspiration, then staring at a blank page trying to write in their own voice.

This pipeline removes research and writing entirely. The only manual steps left are **shoot and upload**.

It's run successfully and produced real scripts used for real videos.

---

## What it does

Every Sunday at 8AM, automatically:

1. **Agent 1 + 1B — Trend Scrapers** pull the top 20 trending YouTube videos (general + niche category) for a target region
2. **Format step** merges and cleans the trend data into a readable list
3. **Agent 2 — Viral Content Analyst** identifies the top 5 trending videos, explains *why* each went viral, what niche it belongs to, and scores its replication potential for your specific content
4. **Agent 3 — Script Ghostwriter** writes a complete 60-90 second script in **your defined voice and philosophy** — structured with timing, stage directions, filming mood, B-roll ideas, and music vibe
5. **Agent 4 — Hook Generator** produces 5 hooks across distinct emotional categories (observation, question, contradiction, relatable tension, poetic) with a recommended top pick
6. **Output** — everything is compiled into a single formatted email, delivered to your inbox

---

## The part that actually matters: the prompts

Anyone can wire up an API call. The real work is in **Agent 3 and Agent 4** — getting Claude to consistently sound like one specific person rather than generic AI output.

This requires defining a **voice profile** for your creator:
- Core stance — how they approach topics (e.g. "never takes sides," "always opinionated," "data-first")
- Audience definition — who they're speaking to and what tension/need that audience has
- Tone constraints — explicit do's and don'ts (e.g. "warm, never preachy")
- Structural rules — a consistent script arc with timing
- Hook philosophy — what makes a hook feel "on brand" vs generic clickbait

The template in this repo includes placeholders (`[CREATOR NAME]`, `[NICHE]`, voice profile sections) — fill these in with your own creator's details and the output quality will reflect how specific you make that profile.

---

## Setup

1. Import `content-pipeline-template.json` into n8n (self-hosted or cloud)
2. Add your credentials:
   - YouTube Data API v3 key
   - Anthropic API key
   - Gmail OAuth2 credentials
3. Fill in the voice profile placeholders in Agent 3 and Agent 4 prompts with your creator's actual philosophy
4. Update the region code and category ID in Agents 1/1B for your target niche
5. Activate the workflow — it runs every Sunday at 8AM automatically

---

## Stack

- **n8n** — workflow orchestration (self-hosted recommended)
- **Claude API** — content analysis, scriptwriting, hook generation
- **YouTube Data API v3** — trend data
- **Gmail API** — delivery

---

## Status

Proven — this exact architecture has produced real scripts used for real recorded videos. Currently being migrated to self-hosted n8n.

---

## Get in touch

Want this built for your own content, in your own voice?

→ [zerohand.dev](https://zerohand.dev)
→ hello@zerohand.dev
