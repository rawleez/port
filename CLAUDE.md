# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project

Personal portfolio website for Rawle. Single page, single scroll — no multi-page
routing, no CMS, no unnecessary complexity. Built in TypeScript by choice (the
user wants the practice and plans to keep using it going forward), not because
the project demands it.

## Status

Repo is currently empty of code — nothing has been scaffolded yet. The user
still plans to share a reference portfolio site to click through for
layout/style inspiration before the first scaffold is built. Update this file
once the stack is chosen and the project structure exists (framework, folder
layout, build/dev/lint commands, deployment config).

## Content

Four source PDFs in the repo root (`port- Intro.pdf`, `Port- AI:Product
Expertise.pdf`, `Port- Featured work.pdf`, `port- Experience.pdf`) hold the
copy for the site's four scroll sections, in that order. Their content is
reproduced below so it doesn't need to be re-read from the PDFs each session.
Treat these PDFs as the source of truth if this section and the files ever
disagree — re-read them and update this file.

### 1. Intro

**Rawle Paul** — product builder exploring AI systems + context-aware
applications

> I build AI-driven products that connect disparate data sources, understand
> user context, and empower people to make better decisions.
>
> I am interested in the kaleidoscopic area between product, data, and
> machine learning, especially problems where the data is already available
> but the connections have not been made to make a special customer
> experience.

### 2. AI/Product Expertise

**Agentic AI + LLM Applications** — I build AI workflows using agents, LLMs,
and automation to reduce manual processes and create frictionless user
experiences.
Experience: agentic pipelines, MCP servers, Gemini / AI agents, LLM-based
workflows.

**Predictive Systems + Analytics** — I work on problems where historical data
can help predict future outcomes.
Experience: forecasting, anomaly detection, operational analytics, data
pipelines.

**Context-Aware Product Design** — I enjoy designing products that
understand more than explicit user input.
Examples: behavioral patterns, personalization, intelligent recommendations,
smart notifications.

### 3. Featured Work

**Find My+** — Context-aware notifications
- *Problem:* Current Find My notifications rely primarily on physical
  separation and location. But a device being left behind doesn't always
  indicate a problem — users bring different devices to different daily
  routines and destinations.
- *Approach:* Designed a context-aware notification model that learns device
  behavior across locations, routines, and time, building a behavioral
  profile so the system can classify whether a missing device is expected or
  unusual (e.g. MacBook missing during a commute → likely important; iPad
  left at home → expected; iPad traveling alone to an unknown location →
  potential anomaly). Combines signals like significant locations, navigation
  destinations, Bluetooth proximity, time of day, and historical movement
  patterns.
- *Impact:* Transforms Find My from a location-based alert system into a
  predictive assistant that understands user intent, reducing unnecessary
  notifications while surfacing situations that actually matter.

**Melody** — AI-powered career discovery
- *Problem:* Traditional job search requires users to translate their
  experiences and goals into keywords.
- *Approach:* Built an AI agent that understands how candidates describe
  their work, extracts preferences and hard limits, and connects those
  signals to relevant opportunities in a natural way.
- *Impact:* A more personalized approach to discovering career opportunities.

**Generation Nest** — Predictive maintenance for smart buildings
- *Problem:* Building maintenance is reactive — problems are discovered only
  after something fails.
- *Approach:* Designed an AI platform combining IoT sensors, machine
  learning, and maintenance workflows to identify issues before failure.
- *Impact:* A proactive maintenance system improving resident experience and
  operational efficiency.

**Wispr Flow Smart Attribution** — Context-aware knowledge capture
- *Problem:* Transcription captures information but often loses the
  surrounding context.
- *Approach:* Designed a feature concept that uses time, location, source,
  and speaker information to automatically organize captured knowledge when
  relevant.
- *Impact:* A smarter way to transform conversations into usable information.

### 4. Experience

**Amazon** — Operations
Building analytical and AI-driven workflows to help operational teams move
from reactive decisions toward predictive insights.

**Apple** — Product Experience
Helped customers navigate technology decisions through product expertise and
communication.

## Design reference

Reference site: https://ijya.vercel.app/ (shared by the user for layout/style
inspiration — not to be copied verbatim, just as a structural/tonal model).

- **Stack observed:** no framework — static HTML/CSS + a single `script.js`.
  No React root, no `__NEXT_DATA__`. Confirms a plain Vite + TypeScript
  (vanilla-ts template) baseline is the right level of simplicity to match.
- **Fonts:** `Outfit` (sans-serif) for nav/body text; `Cormorant Garamond`
  (serif) for section headings — deliberate serif/sans contrast.
- **Palette:** dark theme, alternating section backgrounds between near-black
  (`#1c1c1c`-ish) and a dark plum-brown (`#2e2422`-ish); muted dusty-rose and
  sage-green used as small accent chips/icons.
- **Structure:** sticky centered top nav (about / expertise / featured work /
  connect) → hero (name + tagline + bio, "SCROLL" cue with a vertical line) →
  2-column card grid for the expertise section → featured-work section as
  full-width cards, each pairing a small left-side flow-diagram (colored
  boxes connected by arrows, e.g. step → step → step) with
  problem/approach/impact copy on the right → simple centered footer CTA.
- **Featured Work decision:** no flow-diagrams and no fabricated metrics.
  Render problem/approach/impact as plain text blocks (bold labels, like the
  Content section already has) — do not invent numbers that aren't in the
  source PDFs.

## Deployment

Vercel. Zero-config for a static Vite build, free tier, instant preview URLs
on push — simplest path for a static single-page site. Cloud Run was the
alternative but isn't needed unless requirements change (e.g. needing a
server).

## Working style for this project

- Keep it simple: one scroll page, minimal dependencies, no premature
  abstraction for a site this small.
- TypeScript throughout, including any tooling/config scripts.
- Prefer the simplest stack that satisfies "single scroll-page portfolio in
  TypeScript" — don't reach for a heavier framework than the page needs.
