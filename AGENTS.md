# AGENTS.md

## What this is

Static personal website for Xiangyu Wang, deployed via GitHub Pages. No build system, no framework, no package manager, no tests.

## Structure

- `index.html` — English homepage (root page served by GitHub Pages)
- `zh-cn/index.html` — Chinese homepage (served at `/zh-cn/`)
- `draft_prompt.md` — Chinese-language content drafting notes (not deployed)
- All CSS and JS are **inline** in each HTML file (no external stylesheets or scripts except Google Fonts)

## Critical: keep both HTML files in sync

`index.html` and `zh-cn/index.html` share identical CSS and nearly identical JS. When editing styles, layout, or navigation behavior, **apply the same change to both files**. The only differences should be content text and the language-switcher links.

## No build or test commands

There is nothing to build, lint, typecheck, or test. Edits are direct HTML/CSS/JS changes committed and pushed to `main`. GitHub Pages serves the repo root.

## Resume links

Resume PDFs are external: `https://xiangyuw1.github.io/resume/latest-en.pdf` and `latest-zh.pdf`. These files are **not** in this repo. Do not attempt to edit or reference them as local files.

## Language switcher

- English page links to `/zh-cn/` for Chinese
- Chinese page links to `/` for English
- The active language is styled with `<span class="active">`, the other is an `<a>` tag

## Editing content

Content lives in the HTML `<section>` elements. Section IDs (`education`, `awards`, `research`, `projects`, `coursework`, `skills`) are used by the sticky nav for scroll-based highlighting. Do not rename them without updating the nav links and JS.

## Style conventions

- Fonts: Inter (body) + Noto Serif (headings), loaded from Google Fonts
- Color palette: neutral grays (`#111`, `#333`, `#555`, `#888`, `#e5e7eb`) with accent blue (`#1a6faa`)
- Max content width: 900px (`.page` class)
- Mobile breakpoint: 600px
