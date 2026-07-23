# AGENTS.md

This repo is a curated, personal link collection for job searching — not a software project. There is no build, test, or lint tooling. The only real content is `README.md`.

## Repo structure

- `README.md` — the entire deliverable. A set of `##`/`###` sections, each containing a flat bullet list of links.
- No other source files are expected. Don't add scaffolding (package.json, CI config, etc.) unless explicitly asked.

## Current sections in README.md

- **Remote Jobs Available** — job boards/company career pages with remote listings
- **General Jobs** — broader job boards, not remote-specific
- **Code to Help With Job Search** — open-source tools/repos
- **Tools** — non-code, hosted job-search aids (SaaS, browser extensions), e.g. application autofillers and email finders
- **Training** — subsectioned by topic (e.g. `### AWS Certification`), which may further break down into labeled groups (e.g. `**AWS Certified Cloud Practitioner (Foundation)**`, `**Projects**`) using bold text as a sub-heading, not a markdown heading level
- **Videos** — YouTube links
- **Articles** — blog posts, guides, social posts

New sections/subsections follow this same pattern: `##`/`###` for real headings, bold (`**Text**`) for a lightweight grouping label within a section.

## Link entry format

Every job-board/site/tool entry follows:

```
- [Link Text](url) — **Tag1** · **Tag2** — Short description.
```

- **Link text**: the site/resource name, not the raw URL.
- **Tags**: bolded, separated by ` · ` when there's more than one. The two recurring tag types:
  - Cost: `**Free**`, `**Freemium**`, or `**Paid/Subscription**`. Add a short parenthetical if the free tier is notably limited, e.g. `**Freemium** (paid needed for full catalog)`.
  - Remote availability (mainly under "Remote Jobs Available" and "General Jobs"): `**Remote: Yes**`, `**Remote: Some**`, `**Remote: Many**`.
  - Single-company careers pages get `**Free** (single-company page)` instead of a remote-jobs-catalog framing.
- **Description**: one sentence (occasionally two, separated by `;`), stating what the site/tool is, plus any relevant angle (e.g. altruism/nonprofit focus, startup-only, AI-powered matching).

Videos and Articles entries drop the cost/remote tags (unless the article is explicitly a paid resource) and instead get a short 1–2 sentence summary of the content itself.

## Adding a new link

1. Determine the correct section (create a new `##`/`###` section only if none of the existing ones fit — ask the user if unsure).
2. Research the site/resource before writing the description — don't guess. Use `WebFetch` on the URL, or `WebSearch` if the site blocks fetching (Reddit and LinkedIn both return 403/429 to `WebFetch`; fall back to `WebSearch` for those). If the destination truly can't be verified, say so rather than fabricating specifics.
3. Determine free/paid status and remote-jobs availability from the research, not assumption — several sites here are freemium with real paywalls (e.g. Remotive, VirtualVocations), and getting this wrong defeats the point of the tag.
4. Match the existing bullet format exactly (see above) and place the new bullet in the same relative position/order style as its neighbors (no enforced alphabetical or other ordering currently — new entries are typically appended to the end of their section/subsection).

## Git workflow

- Only commit when the user explicitly says so (e.g. "commit and push"); don't commit automatically after every edit.
- Only push when the user explicitly asks to push.
- Use a single-purpose commit per user request (e.g. "Add X to Y section") — don't bundle unrelated changes.
