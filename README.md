# freeflowlab.com

The FreeFlow Lab marketing site. A single self-contained HTML file, served by GitHub Pages.

**Live:** [freeflowlab.com](https://freeflowlab.com)

---

## Editing

The whole site is `index.html`. There is no build step. Commit to `main` and the change is live in about thirty seconds.

**In the browser, no git required:** open `index.html` here on GitHub, click the pencil icon, edit, then "Commit changes."

**Locally:**

```bash
git clone https://github.com/freeflow-lab/freeflowlab-website.git
cd freeflowlab-website
# edit index.html, open it in a browser to preview
git add index.html && git commit -m "describe the change" && git push
```

Opening `index.html` directly in a browser renders it exactly as it will appear live.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site. Structure, styles, and scripts in one file. |
| `Keenan.png`, `Chris.jpeg`, `Siphiwe.jpeg` | Founder photos, referenced by relative path. |
| `og-image.png` | 1200x630 card shown when the link is shared on LinkedIn, Slack, iMessage. |
| `favicon.svg`, `apple-touch-icon.png` | Browser tab and home-screen icons. |
| `CNAME` | Created by GitHub when the custom domain is set. Do not delete. |

## Structure

The site presents four intelligence lines: **Revenue**, **Finance**, **Workforce**, and **Operations**, plus a Solutions Hub that ties them together.

It also carries deliberate Answer Engine Optimization work: a "Summarize with AI" control that hands a pre-shaped prompt to an LLM, and a proof-of-customers module near the top of the page.

## Known gaps

- **Contact forms are not wired to a backend.** Every `<form>` uses `onsubmit="event.preventDefault()"`, so submissions go nowhere. These need to point at the GoHighLevel form endpoint before the site can capture leads. Until then the site is strictly worse at lead capture than what it replaced.
- **The proof-of-customers module is empty.** Dashed placeholder slots render as unfinished. Populate with client logos or case studies.
- Social links in the footer point at generic `linkedin.com` and `youtube.com` rather than FreeFlow Lab profiles.
- `og-image.png` was generated with a fallback typeface rather than Inter. Regenerate if the brand font matters at that size.

## Conventions

- Keep it one file. If it outgrows that, split into pages rather than adding a build step.
- Two people editing the same file will eventually hit a merge conflict. Say something in chat before a large edit.
- Brand palette is defined in the CSS variables at the top of the file. Change colors there, not inline.

---

*FreeFlow Lab. Free the work. Free the people.*
