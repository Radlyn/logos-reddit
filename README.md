# Logos

A personal, local-first tool for surfacing divisive Reddit threads and responding with relevant philosophical quotes — with the goal of encouraging reflection and lowering the temperature of online political discourse.

**Nothing posts to Reddit without explicit human review and approval.** Logos is a decision-support tool, not an autonomous bot.

---

## What it does

1. **Monitors Reddit** — Periodically scans a configured list of subreddits for threads that score highly on a divisiveness rubric you define. Filters by comment count, score, and topic.

2. **Analyzes threads** — Uses the Anthropic Claude API to score each thread's divisiveness (0–10), summarize the nature of the conflict, and extract philosophical themes (e.g. "epistemic tribalism", "us-vs-them framing").

3. **Recommends quotes** — Matches 3–5 quotes from a curated corpus of ~500 philosophical texts (Stoics, Greeks, Enlightenment thinkers, Eastern philosophy, modern political philosophy) to the thread's themes. Each recommendation includes an AI-generated note explaining its specific relevance to that thread.

4. **You review** — A private web UI presents pending threads sorted by divisiveness score. You expand a thread, read the summary, browse the quote recommendations, select one, optionally edit the framing note, and approve — or dismiss.

5. **Posts** — On your approval, Logos posts a single comment to the thread under your Reddit account.

---

## Design principles

- **Human in the loop, always.** The agent never posts autonomously. Every post requires your explicit approval in the UI.
- **Low volume by design.** The tool is built for thoughtful, infrequent engagement — not bulk posting.
- **Local-first.** Runs entirely on your machine. No cloud infrastructure, no third-party data storage.
- **Transparent.** Posts are made under your own Reddit account. Nothing is anonymous or disguised.
- **Configurable.** The divisiveness rubric, threshold, topics, filters, and subreddit list are all editable in the UI without touching code.
