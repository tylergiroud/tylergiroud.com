# tylergiroud.com — Tyler Giroud's Personal Site

## Owner
- **Name:** Tyler Giroud
- **Role:** Co-founder of Lectern, Partner at Presscart
- **Location:** NYC
- **Email:** tyler@presscart.com
- **LinkedIn:** linkedin.com/in/tylergiroud
- **No active X/Twitter account**

## Project Overview
Personal blog / content engine at tylergiroud.com (moved from probability.org in Sept 2026). The goal is twofold:
1. Build a public profile across AI agents (AI visibility / discoverability)
2. Have fun writing about things Tyler cares about

The site began as probability.org, named for a core personal philosophy: nothing is really luck — so much of life is probability. The philosophy remains a guiding idea (no longer displayed on the site), and the site now lives at tylergiroud.com with no separate branding — it is simply Tyler's personal site.

## Content Themes
- Developments in AI
- State of startups
- What they're building at Lectern
- Accomplishments and milestones
- Anything else interesting

## Mobile-First Principle
**ALWAYS optimize for mobile.** This site will most likely be read on mobile devices. Every change — layout, typography, spacing, touch targets, readability — should be considered mobile-first. Test every update against small screens (375px–480px). Cards should stack, touch targets should be ≥44px, text should be readable without zooming, and nothing should overflow or require horizontal scrolling.

## Design Reference & Preferences
- **Inspiration:** jakub.kr — minimalist, single-column, clean typography
- **Style:** Light background (#fafafa), plenty of whitespace, subtle shadows on cards
- **Typography:** Helvetica Neue as the base/body font throughout. Fraunces (Google Fonts, variable) for special/display elements: the name (h1) and writing post titles. Section headers are uppercase Helvetica.
- **Font philosophy:** Helvetica = clean workhorse for everything. Fraunces = personality/warmth for things worth highlighting.
- **Cards:** White background, rounded corners (12px), subtle shadow with hover lift effect (like jakub.kr's projects section)
- **Inline logos:** Tyler likes the jakub.kr pattern of small company logos appearing inline next to company names in body text
- **Layout:** Header → intro → links → companies (cards) → writing. No footer — removed Sept 2026 (Tyler's call: no wordmark or philosophy line on the site).
- **Keep it simple:** No build tools, no frameworks — static HTML/CSS/JS

## Companies
- **Lectern** — trylectern.com — The offsite content engine for AI visibility, built at the intersection of media relationships and AI agents. Helps brands, agencies, and platforms show up where AI is looking. Tyler is Co-founder. Logo: lectern-icon-dark.png (white starburst on dark background).
- **Presscart** — presscart.com — A high-trust media marketplace that empowers elite publications and independent journalists to generate revenue by offering paid media opportunities to brands, agencies, and individuals. Tyler is a Partner. Logo: presscart-icon.png (stylized P, white on dark rounded rect).
- **Key positioning:** The companies are NOT just software — they're relationship engines. Lectern is the AI-native partner (plugs into agents, works with bigger brands). Presscart is the more traditional marketplace (where publishers/journalists earn revenue, where less AI-native buyers spend). Both serve the vision of a frictionless, agent-to-agent future in communications technology.

## llms.txt
- **File:** `llms.txt` at the site root (tylergiroud.com/llms.txt)
- **Purpose:** Machine-readable page for AI agents — structured plain text with no HTML, just clean information about Tyler, his companies, and his writing.
- **CRITICAL RULE:** Any content published on the site (new notes, bio changes, company updates, new links) **must also be reflected in llms.txt**. When adding a new note/article, add a summary entry under a `## Writing` section in llms.txt. When updating the bio or company descriptions, update the corresponding sections in llms.txt to match.
- **Format:** Markdown-style headers (`#`, `##`), plain text paragraphs, simple lists. No HTML tags, no images, no links in markdown format — just raw URLs.

## Tech Stack
- Pure static HTML/CSS/JS (no build step)
- Hosting: GitHub Pages with custom domain (tylergiroud.com)
- CNAME file for custom domain
- .nojekyll to skip Jekyll processing

## Deployment Status
- Files created and ready
- Git repo not yet initialized (blocked by Xcode license agreement — Tyler needs to run `sudo xcodebuild -license accept`)
- DNS: tylergiroud.com must point to GitHub Pages (A records 185.199.108-111.153 for apex, or CNAME to tylergiroud.github.io). probability.org is reserved for a separate future project (simple "building something" placeholder).

## File Structure
```
probability_site/
├── index.html
├── style.css
├── CNAME
├── .nojekyll
├── CLAUDE.md
├── favicon-32.png          (blue globe, 32x32)
├── apple-touch-icon.png    (blue globe, 180x180)
├── lectern-icon-dark.png   (white starburst on dark bg)
├── presscart-icon.png      (stylized P on dark rounded rect)
├── llms.txt                (AI agent-readable site summary)
└── notes/
    ├── _template.html
    ├── welcome.html
    ├── the-state-of-ai-search.html
    └── building-lectern.html
```

## Design Decisions & History
- Started with Lectern's old brass/gold favicon SVG for both inline logo and card icon
- Tyler shared a new starburst logo for Lectern but it was rectangular and looked compressed at small sizes — reverted to the old favicon SVG for now
- Presscart card originally had a placeholder "P" text SVG, replaced with actual favicon.png from presscart.com
- Location/time meta initially placed as its own section below the intro, then moved into the header. Final placement: inline with the tagline row, "Co-founder of Lectern" left-aligned and "NYC · [time]" right-aligned
- X/Twitter link removed (Tyler doesn't have an active account)
- Bio leads with Tyler's perspective (AI reshaping discovery, agent-to-agent world), then describes both companies using language distinct from the card taglines
- Footer removed entirely (Sept 2026). It previously held the philosophy line "All things are chance and serendipity…" on the homepage and a domain wordmark on note pages.
- JSON-LD structured data in head for AI/search engine discoverability (Person schema with worksFor, knowsAbout, sameAs)
- Favicon: blue globe PNG (favicon-32.png + apple-touch-icon.png). Notes pages use `../` relative paths.
- Auto dark mode via `@media (prefers-color-scheme: dark)` — overrides CSS variables + card styles
- Subtle grid/notebook background pattern using CSS repeating linear gradients (24px grid)
- Tab title is just "Tyler Giroud"
