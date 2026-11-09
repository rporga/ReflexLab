# Reflex Lab

**Reflex Lab** is an independent cultural intelligence passion project. Research any keyword, interest or topic, inspect public conversations and news coverage, understand recurring themes, and develop testable strategic opportunities.

**Live website:** https://reflex-lab-rustyorga-2076.vercel.app

## What this first version does

- Explore up to three comma-separated topics or keywords.
- Add a research audience, objective and terms to exclude.
- Search a 7-day or 30-day window using public Bluesky post search and GDELT news coverage.
- Keep evidence linked to its source, with source-specific availability warnings.
- Identify repeated words, lightweight theme classifications, and directional sentiment cues.
- Turn observed themes into **hypotheses and suggested experiments**, not ungrounded market claims.
- Export research snapshots as JSON and evidence lists as CSV.
- Browse a **synthetic demo**, clearly labelled as fictional data.
- Use separate Overview, Cultural Signals, Conversations, Opportunity Lab and Methodology tabs.

## Architecture

| Path | Role |
| --- | --- |
| public/index.html | Dashboard layout and metadata |
| public/assets/styles.css | Responsive styles |
| public/assets/app.js | Research form, tabs, charts, report views and exports |
| api/explore.js | Serverless API, public-source retrieval and transparent theme analysis |
| vercel.json | Static frontend output configuration |
| package.json | Node project metadata |

The frontend is plain JavaScript and CSS, so there is no build step or dependency-heavy framework. Vercel serves the public directory and invokes api/explore.js as a Node.js Function.

## GitHub & Vercel

Repository: https://github.com/rporga/ReflexLab

Vercel project: **reflex-lab** under **rustyorga-2076's projects**.

Pushing to the main branch automatically creates a new production deployment. Previews can be deployed from non-production branches.

## Public-source methodology

Bluesky search is *not* a complete feed of every relevant post. GDELT indexes news coverage, not a social-platform conversation firehose. Our results are limited retrieved samples and should never be presented as full-market prevalence, historical trend growth, statistically valid sentiment or demographic profiles.

Themes and tone currently use simple rule-based token matching. Opportunities are research hypotheses worth testing. **Forecasting is deliberately marked unavailable** until we have continuously collected longitudinal data, reliable benchmarks and backtesting.

## Next milestones

1. Add a source collection database and regularly sampled history.
2. Improve language clustering with embeddings and properly cited AI-assisted summaries.
3. Develop signal momentum with uncertainty and source-normalised baselines.
4. Add approved additional social integrations and platform-aware data governance.
5. Add saved research workspaces, recurring monitors and evaluation of forecast accuracy.

## Privacy and boundaries

Reflex Lab is an independent personal project. It uses no proprietary WPP code, internal agent prompts, work datasets or credentials. The app only requests public data through supported endpoints; it does not bypass logins, access private posts or claim that any person belongs to a particular demographic.

Please respect platform terms, source deletions, privacy law and rate limits before publishing or commercialising derived results.

## Current status

Prototype live on Vercel. Homepage, frontend assets and API route have been verified to respond successfully; live data connectors may still be limited by provider availability or rate limits.
