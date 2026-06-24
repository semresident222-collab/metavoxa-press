# MetaVoxa Press

**press.metavoxa.com** — Where lived experience becomes language.

> MetaVoxa Press is the public voice of MetaVoxa. Essays, vocabulary, and the recurring editorial gesture of the Star of the Month. The place where observation becomes language before it becomes anything formal.

---

## What This Is

MetaVoxa Press is a literary publication, not a blog. It holds three distinct sections, each with a different job and a different register. They share a design language but not a mood, moving between them should feel like moving between rooms in the same institution, not between tabs on the same dashboard.

---

## The Three Sections

### 01 — Dispatches (`index.html`)
Essays from the edge of systems, selfhood, medicine, and meaning.

Cards with title and short summary live here. Full essays are read on Substack. This page is the editorial index — discovery, not reading. Updated monthly as new essays are published.

**Substack:** https://substack.com/@metavoxapress

**Categories:** SELFHOOD · SYSTEMS · MEDICINE · NEURODIVERGENCE · RELATIONSHIPS · INFRASTRUCTURE

**Current count:** 12 published dispatches (as of June 2026). To add a new dispatch: append a new object to the `DISPATCHES` array in `index.html`. The page renders from the data — no HTML editing needed.

---

### 02 — Star of the Month (`star-of-the-month.html`)
Full story. Hosted here. Not on Substack.

This is the editorial centrepiece of the publication. One person per month. Full portrait, full story, the pull-moment-to-deepen mechanic, the constellation archive. This is the one section that lives entirely on Press rather than linking elsewhere.

**Migrated from:** MetaVoxa Atrium (where it previously lived as a standalone page). The navigation has been updated to point within the Press ecosystem rather than back to Atrium.

**To update for a new month:**
- Replace `diana-portrait.jpg` with the new portrait (same filename, or update the `src` attribute)
- Update the name, date, location, pull moment, quote, and context note in the HTML
- Add the previous star to the archive timeline in the modal

---

### 03 — The MetaVoxa Lexicon (`lexicon.html`)
The language index for realities systems have not learned to name.

A living dictionary. Full term detail panel — definition, field note/origin, where it appears, why it matters, related terms. Alphabetical index, category filter, search. Two-panel layout: term cards left, term detail right.

**Current count:** 22 terms across Tier 1 (Constitutional), Tier 2 (Native Concepts).

**Term coding system:** Letter prefix of term name + sequential number (e.g. I-001 for Interpretative Sovereignty, P-022 for Performed Wellness). Matches the numbering visible in the mockup.

**Tiers:**
- **Tier 1 — Constitutional:** Core terms that define how MetaVoxa perceives reality (Observation, Signal, Noise, Translation, Visibility, Adaptation, Human Cost, Evidence, Lived Experience, Autonomy).
- **Tier 2 — Native Concepts:** Terms coined by MetaVoxa that do not exist in conventional vocabulary (Performed Wellness, Masking Load Index, Adaptation Cost, etc.).
- **Tier 3 — Ecosystem Terms:** Operational infrastructure names (MetaVoxa Labs, The Observatory, etc.) — not yet in the Lexicon, added in a future update.

**To add a new term:** append a new object to the `TERMS` array in `lexicon.html`. The page renders from the data — no HTML editing needed. Assign the next sequential number for that letter prefix.

**Motto:** VERITAS PER VOCEM — truth through voice.

---

## File Structure

```
press.metavoxa.com/
├── index.html              — Dispatches (main landing page)
├── lexicon.html            — The MetaVoxa Lexicon
├── star-of-the-month.html  — Star of the Month
├── archive.html            — Press Archive (future)
├── featured-dispatch.jpg   — Hero image for featured dispatch card
├── lexicon-hero.jpg        — Hero image for Lexicon page (open book)
└── diana-portrait.jpg      — Current star portrait (update monthly)
```

---

## Image Assets

| File | Description | Used in |
|------|-------------|---------|
| `featured-dispatch.jpg` | Open journal/notebook, dark surface, amber candlelight, literary atmosphere | Dispatches — featured card right column |
| `lexicon-hero.jpg` | Ancient open tome on dark desk, globe, brass instruments, warm candlelight | Lexicon — full-width hero section |
| `diana-portrait.jpg` | Portrait of current Star of the Month | Star of the Month page |

All images degrade gracefully — if a file is missing or fails to load, the relevant section falls back to a dark styled placeholder. Nothing breaks.

---

## Design Language

**Typography:** Cinzel (wordmark, navigation, labels, metadata) · Cormorant Garamond (body, descriptions, pull moments) · Playfair Display (display headlines, hero titles)

**Palette:** Near-black warm base `#0d0c09` · Antique gold `#C9A461` · Cream paper cards `#F5F0E8` · Ink on cards `#1A1410`

**Grain overlay:** Fixed, low-opacity SVG noise texture on all three pages — creates the aged-paper, literary atmosphere. Present on all pages.

**Design logic:**
- Dispatches: dark base, cream paper cards, editorial and scannable
- Star of the Month: cinematic, intimate, dark navy/gold, immersive — deliberately the most atmospheric surface in the Press
- The Lexicon: dark base, open book hero, two-panel reference interface — scholarly, precise

The Star of the Month is intentionally the tonal outlier — its atmosphere should feel like a different room, not a different palette. This contrast is a feature, not an inconsistency.

---

## Content Source of Truth

All copy in this site derives from the **MetaVoxa Knowledge Core** — specifically:

- **Press Database** (essays, trigger events, branching outcomes) → Dispatches
- **Vocabulary document** (Tier 1, 2, 3 definitions) → The MetaVoxa Lexicon
- **Community Signals** (Star of the Month — real people, real stories)

**The Fortress Principle applies:** if content here and the Knowledge Core disagree, the Knowledge Core wins. This site is an output. Update the Core first, then update the site.

---

## Ecosystem Position

```
metavoxa.com  (neutral landing — front door)
   ├── atrium.metavoxa.com   — sovereign digital estate
   ├── labs.metavoxa.com     — research infrastructure
   ├── press.metavoxa.com    — THIS REPO — public voice
   ├── research.metavoxa.com — publications and academic record (future)
   └── marthakoroma.com      — founder threshold (external)
```

Press is one room. It does not explain the others. `metavoxa.com` is the front door.

---

## Maintenance Cadence

| Task | Frequency | File |
|------|-----------|------|
| New dispatch published | Monthly (or as published) | `index.html` — append to `DISPATCHES` array |
| Star of the Month update | Monthly | `star-of-the-month.html` — update content, add previous star to archive |
| New Lexicon term | As coined | `lexicon.html` — append to `TERMS` array |
| Social links (X, TikTok) | When consistently active | Add to footer across all pages |

**TikTok and X/Twitter** are deliberately absent from the current build. Both accounts exist but are not yet posting consistently. They will be added to the footer across all pages once active — not before.

---

## Deployment

- Domain: `press.metavoxa.com` → this repo (CNAME record at DNS provider)
- [Add your actual host/build details here — GitHub Pages, Vercel, Netlify, etc.]

---

*Maintained by Martha Wuya Koroma. Part of the MetaVoxa Knowledge Core ecosystem.*
*Last updated: June 2026*
