# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

## What this repo is

The public marketing + legal site for the LEAF cigar journal iPhone app, served at
**leafcigars.fyi** (GitHub Pages; `CNAME`). Static hand-written HTML, no build step —
open a page in a browser to check it.

- `index.html` — landing page. Self-contained `<style>` block; the phone mockups are
  hand-built HTML, not screenshots.
- `privacy.html`, `terms.html` — the legal pages. They share `leaf.css`.
- `pa.js` — PostHog snippet loaded by every page (disclosed in Privacy Policy §11).

## Rules

- **The app is the source of truth for both the mockups and the legal copy.** The LEAF
  app repo (`~/firstmate/projects/LEAF`, a sibling clone) is READ-ONLY from here: its
  `CLAUDE.md` guardrails, `src/lib/analytics.ts` allow-list, `src/lib/region.ts`, and
  the Cedar surfaces under `src/app/` / `src/components/cedar/` are what these pages
  describe. Never edit that repo from this one.
- **The mockups must depict shipped screens, and only shipped screens.** Copy the Cedar
  tokens (`src/theme/tokens.ts`) rather than inventing colours, and never illustrate a
  feature, claim, or catalog fact the app does not have.
- **These legal pages back the App Store privacy disclosures** and are the app's only
  legal copy — the app links to them (`src/app/(tabs)/you/settings.tsx`) and deliberately
  ships no in-repo legal text. A data-practice change in the app is a change here.
- **Legal wording is a captain decision.** Draft changes and flag every legal/business
  judgment call in the PR body; do not merge legal copy without captain review. Bump the
  effective date + version line when the substance changes.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
