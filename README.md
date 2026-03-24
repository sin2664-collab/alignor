# alignor.md

**A single markdown file that turns any LLM into your alignment guardian.**

Paste it into Claude Projects, ChatGPT Custom Instructions, or Cursor rules.  
No install. No API key. No setup.

---

## The problem

AI makes you 100x faster.

But if your direction is off by 1 degree, you end up 100x further from where you wanted to be.

You've been there: shipped a ton of stuff, checked every task off the list —
then looked up and realized none of it moved the needle on what actually mattered.

This is the **Productivity Paradox** of the AI age.  
Speed without alignment is just accelerated drift.

---

## What alignor does

You define your **mission** (why you exist) and **visions** (concrete future states you're aiming for) once.  
Every task your LLM generates gets tagged, scored, and checked against your visions.  
Drifted items get flagged.

```
[TASK] Re-engagement newsletter to inactive users
[WHY]  Recovers lapsed users — directly moves V1 forward
[VID]  V1
[OUT]  +15% retention among inactive segment within 30 days
[PRI]  HIGH

[TASK] Reorganize internal Notion workspace
[WHY]  Operational tidiness — no connection to any vision
[VID]  NONE
[OUT]  Cleaner workspace
[PRI]  LOW

─────────────────────────────────────
ALIGNMENT CHECK
─────────────────────────────────────
V1 (grow active user base):  [████████████████░░░░]  82/100  ✓
V2 (launch in new market):   [░░░░░░░░░░░░░░░░░░░░]   0/100  — no tasks this week

MISSION COHERENCE:           [████████████████████] 100/100

DRIFTED:
  ✗ Reorganize Notion — operational, moves no vision forward

VERDICT: PARTIAL
V1 is well-covered. Nothing moved V2 this week — intentional, or crowded out?
─────────────────────────────────────
```

---

## Mission vs Vision — why both matter

Most tools conflate these. alignor keeps them separate on purpose.

| | Mission | Vision |
|---|---|---|
| **What it is** | Why you exist | Where you're going |
| **Changes?** | Never | Yes — as strategy evolves |
| **Abstraction** | High | Concrete and observable |
| **Role in alignor** | Background context | The actual scoring target |

A task that "feels aligned with the mission" but serves no vision is still **DRIFTED**.  
Visions are the scoring targets. Mission validates that your visions are pointing the right way.

---

## Setup (5 minutes)

**1. Download [`alignor.md`](./alignor.md)**

**2. Fill in Section 1 — Mission**

Use the fill-in-the-blank structure:

```
We exist to [core purpose].
We believe [fundamental belief others might disagree with].
We will never [what you refuse to do, even for money].
```

**3. Fill in Section 2 — Visions**

Use the fill-in-the-blank structure:

```
V1: By [timeframe], [who] will [do or experience what].
V2: By [timeframe], [who] will [do or experience what].
```

**4. Paste the whole file into your LLM**

Done. Every conversation from now on is alignment-aware.

---

## Works with any LLM

| Tool | Where to paste |
|------|----------------|
| Claude Projects | System Prompt |
| ChatGPT | Custom Instructions |
| Cursor | `.cursor/rules` |
| Windsurf | `.windsurfrules` |
| Gemini Gems | Custom Gem instructions |
| n8n / MCP | First system context node |
| Any API | `system` parameter |

---

## Why a markdown file?

No SaaS to sign up for. No data leaving your machine beyond what you already send your LLM.  
No workflow changes. Just a file you own, control, and can edit in 30 seconds.

> The file is the product.

---

## FAQ

**Isn't this just prompting an LLM?**  
Yes. The value isn't the technology — it's the structure. Most people have a mission in their head. Few have one legible to their tools. The fill-in-the-blank format forces enough specificity for scoring to actually mean something.

**Why score against visions, not the mission?**  
Mission is too abstract to score against reliably. "Does this task serve our purpose?" — an LLM will say yes to almost anything. "Does this task move V2 forward?" — that's concrete enough to score honestly.

**Can't anyone copy this?**  
Yes. The templates, community configs, and habit of using it are what compound over time.

**Does this work with GPT-4 / Gemini / Mistral?**  
Yes. Tested with Claude, ChatGPT, and Gemini. Any instruction-following model works.

---

## Roadmap

- [x] v0.1 — single markdown file, works with any LLM
- [ ] v0.2 — CLI: `cat output.txt | alignor check`

---

## Contributing

Most useful contributions right now:

1. **Your config** — what mission/vision format worked for your use case
2. **Template PRs** — your industry's version of alignor.md
3. **Failure cases** — when did scoring feel wrong? Open an issue.

---

*Speed without direction is just accelerated failure.*

MIT License · Made by [@yourhandle](https://github.com/yourhandle)
