---
name: web-research
description: Fast web research using nanobot's built-in web_search and web_fetch tools.
metadata: { "nanobot": { "emoji": "🔎" } }
---

# Web Research

Use this skill for finding reliable, current information from the web.

## When to use

Use when the user asks to:

- Searching for documentation or API references
- Looking up facts or current information
- Fetching content from specific URLs
- Any task requiring web search without interactive browsing

## Tools used

- `web_search`: discover relevant pages
- `web_fetch`: read page contents for analysis

## Workflow

1. **Clarify scope**  
   If the user’s query is broad, narrow to 1-2 focused search intents.

2. **Search first**  
   Call `web_search` with targeted query terms.
   Prefer queries with domain/context keywords (e.g., "official docs", year, product/version).

3. **Pick best sources**  
   Prioritize:
   - official docs/sites
   - primary sources
   - reputable publications

4. **Fetch and verify**  
   Use `web_fetch` on the top 2-5 links to confirm details before answering.

5. **Synthesize**  
   Give a concise answer first, then include source links and key supporting points.

## Output style

- Lead with direct answer in 1-3 sentences
- Then include:
  - `Sources:` list of URLs
  - `Key points:` short bullets
- If sources conflict, state uncertainty clearly and show both sides.

## Guardrails

- Do not invent facts not present in fetched sources.
- If search results are weak, say so and ask whether to refine search terms.
- Prefer recency for news/current events; prefer authority for technical docs.
