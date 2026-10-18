# Daily blog guide (for the scheduled 11 a.m. ET post)

Posts live in `posts.json` → `{"posts": [ ... ]}`. The site renders them automatically
(newest first). Only edit `posts.json`; never edit `index.html` for a post.

## One post per day
- Topic: AI agent adoption — enterprise/government rollout, governance, evaluation, ROI,
  security, workforce and change management, standards/interoperability, real deployments.
- Prefer news and research from the last ~14 days. Do not repeat a topic or headline
  already in `posts.json`; pick a new angle.
- Open (fetch) every page you cite. Use primary or reputable sources (vendor/analyst press
  releases, research reports, major outlets, standards bodies). 2–4 sources per post.
- Never invent numbers or quotes. Every figure in the post must appear in a cited source.

## Voice and length
- Archana Kotaru: AI technical program & delivery leader. Practical, plain, confident.
- 150–250 words in 3–4 short paragraphs: what happened (with figures), why it matters,
  a delivery leader's take, one concrete takeaway.
- Do NOT mention her employer, clients, DoD/DoW programs, or any internal work.
  No job-seeking language. No hype words ("game-changer", "revolutionary").

## Schema (append one object)
```json
{
  "slug": "YYYY-MM-DD-short-kebab-title",
  "date": "YYYY-MM-DD",
  "title": "Short headline, under 80 characters",
  "summary": "One sentence, under 200 characters.",
  "body": ["Paragraph 1", "Paragraph 2", "Paragraph 3"],
  "tags": ["Adoption", "Governance"],
  "sources": [{"title": "Publisher: Page title (Month YYYY)", "url": "https://..."}]
}
```
- Plain text only in strings (no HTML/Markdown). Validate JSON before committing.
- Date = today in America/New_York. If a post for today already exists, do nothing.

## Publish
Commit `posts.json` to `main` with message `Blog: <title>` and push. Vercel deploys
automatically to https://archanakotaru.vercel.app/ within a minute.
