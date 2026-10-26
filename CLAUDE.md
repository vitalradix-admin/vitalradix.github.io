# vitalradix.com — Claude Code instructions

## Project
Static marketing site for Vital Radix (sleep / circadian rhythm brand), hosted on GitHub Pages.
- Repo: vitalradix-admin/vitalradix.github.io
- Live: https://vitalradix.com (custom domain via CNAME)
- No build step, no framework. Plain HTML/CSS/JS.

## Hard rules (site breaks if violated)
- `index.html` must stay at repo root, exactly that name, lowercase.
- Never delete, rename, or edit `CNAME`. It must contain only: www.vitalradix.com
- Keep `.nojekyll` if present. Do not add Jekyll config unless asked.
- Do not change GitHub Pages settings, repo visibility, or branch rulesets.
- Use relative asset paths (`logo.png`), never absolute local paths.
- Asset filenames are case-sensitive on Pages. Match references exactly.

## Workflow
1. Before editing, run `git status` and `git pull`. Confirm the current branch.
2. Make the smallest change that satisfies the request. Do not reformat untouched code.
3. Before committing, validate:
   - `index.html` and `CNAME` exist at root
   - No broken local links: grep every `src=`/`href=` to a local file and confirm it exists
   - HTML is well-formed (balanced tags)
4. Preview locally: `python3 -m http.server 8000` and check http://localhost:8000
5. Commit with a clear message. If a branch ruleset blocks direct pushes to main, open a PR and tell me it must be merged before the change goes live.
6. After pushing, remind me to check the Actions tab for "pages build and deployment".

## Business facts (keep consistent site-wide)
- Sleep Reset book: $15.99
- Foundation Reset Quick Guide: $2.99
- Store: https://stan.store/VitalRadix
- When a price changes, search the whole repo for the old price and update every occurrence (text, meta tags, structured data).

## Brand
- Tone: calm, authoritative, evidence-first. No hype, no exclamation-heavy copy.
- Avoid em dashes and excessive hyphens in copy.
- Palette: deep forest green, parchment/cream, muted copper/gold.
- Fonts: elegant serif (Cormorant Garamond, Libre Baskerville).
- Taglines: "Rhythm before remedies." / "Rooted in biology. Grounded in nature. Built on rhythm."

## Communication
- Be concise. Show diffs, not whole files.
- Ask before deleting files, changing config, or any change outside the request.
- If something could take the site offline, stop and explain first.
