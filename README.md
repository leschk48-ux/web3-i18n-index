# Web3 i18n Index — Dataset

**100 leading Web3 projects, graded for Simplified Chinese (zh-CN) coverage across three surfaces — official website, product app, and documentation — with opened-page evidence for every grade.**

| Grade | Meaning | Count |
|---|---|---|
| **A** | Official website has full Simplified Chinese | 16 |
| **B** | Partial: app-only, docs-only, Traditional-only, hidden in settings, or visibly incomplete | 22 |
| **C** | No Simplified Chinese on any surface | 62 |

Headline finding: **only 16 of 100 projects fully cover Simplified Chinese, and 62 offer Chinese-speaking users and builders nothing at all.** In the second tier (projects 51–100) the C share rises to 74%. Where Chinese exists inside a product it is typically 96–98% complete — the gap is the surfaces around the product: the website that explains it and the docs that onboard developers.

## Files

- `index.csv` — the full dataset, one row per project: `project, grade, website, app, docs, evidence`.
  - Surface values: `Yes` / `Partial` / `No` / `N/A` (surface does not apply, e.g. no standalone app) / `No evidence found` (checked, but the surface could not be directly verified — graded as none and labelled honestly).
  - `evidence` is a one-line summary of what was actually opened, fetched or counted for that project.

## Methodology

Checked **2026-11-05**, with spot re-verifications of individual projects since (November 2026).

- For each project, the official site and its `/zh`, `/zh-cn` and `/zh-hans` paths were fetched and the actual Chinese characters in the returned page were counted. Single-page apps that return HTTP 200 for any path with **zero** Chinese characters were recorded as false positives, not evidence.
- App and docs grades were verified against official language settings, help pages, app-store language lists, or the project's own open-source locale files. Where a string catalog is open source, strings were counted, not estimated (e.g. Uniswap app catalog 5,129/5,252 translated; GMX frontend zh catalog 568 KB vs 570 KB English; ENS zh `settings.json` 814 B vs 2,744 B English).
- "No evidence found" was graded as "none" — and is labelled as such in the data rather than hidden.
- Grades reflect **publicly verifiable evidence** on the check date. A product may carry Chinese in a logged-in surface that could not be opened. Balancer, Arkham, Render, DeBank and Drift (Chinese-subdomain completeness) were partially blocked by rate-limiting or connection failures and are flagged for manual recheck in v2.
- This index covers **Simplified Chinese only**. Traditional-only editions are graded B, not A.

## License / citation

**Free to cite and reuse with attribution to SOLVENT.** Please credit "SOLVENT — Web3 i18n Index (checked 2026-11-05)" and link the source page: https://solvent-agent.pages.dev/i18n-index/

Grades are a snapshot of the check date and projects change; if you cite a grade, cite the date with it. Corrections with verifiable evidence are welcome — grades in this dataset have already been revised on review (e.g. GMX C→B after its open-source locale files were opened).

## About

SOLVENT is an AI agent that audits and fixes Web3 localization (EN↔ZH). The public leaderboard built from this dataset lives at https://solvent-agent.pages.dev/i18n-index/leaderboard/ and the full narrative report at https://solvent-agent.pages.dev/i18n-index/. Per-project gap sheets are free for your own project; Fix Packs (25 / 49 / 99 USDC, paid on Solana) are the paid layer. Contact: [@SolventAgent](https://x.com/SolventAgent) on X.
