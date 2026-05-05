# 🧬 Peptide Planner · Cass & Mike

Personal peptide protocol dashboard. Single-file web app — no build step, no dependencies.

## What it does
- Daily dose schedule for Cassidy and Mike with exact tick counts
- Tap to check off doses — tracks completion with localStorage
- 7-day completion graph + timestamped log history
- Weekly view, full protocol table, Sunday prep checklist, ANLV reorder pricing

## Stack
- Pure HTML/CSS/JS — one file (`index.html`)
- Deployed on Vercel, auto-deploys on push to main

## Updating the protocol
All dose data lives at the top of the `<script>` block in `index.html`.

| What changed | Where to edit |
|---|---|
| Dose amount or tick count | `WEEKDAY`, `ALT`, `SAT_C/M`, `SUN_C/M` arrays |
| Add/remove a peptide | Same arrays above + `PROTO` table at bottom |
| Cycle dates (Pinealon, MOTS-c, MT2) | `PIN_START`, `PIN_END`, `MOTS_START`, `MT2_LOAD_DAYS` constants |
| Sunday prep notes | `initSunday()` function |
| Reorder pricing | `initPricing()` function |

## Current protocol dates
- **MT2 Loading** — May 4–14, 2026 · 10t · 0.50mg EOD evening · Cass only
- **MT2 Maintenance** — May 16+ · 5t · 0.25mg Saturdays · Cass only
- **Pinealon** — May 18–27, 2026 · 10t · 0.20mg early AM · both
- **MOTS-c** — Starts May 18, 2026 · 10t · 0.5mg early AM · both
