<h1 align="center">Khatibullah Rahel</h1>

<p align="center">
  <strong>AI Engineer · Full-Stack · TypeScript</strong><br/>
  Building production AI systems — not wrappers around API calls
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/khatibullahrahel">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://rahel-portfolio-one.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white"/>
  </a>
  <a href="mailto:khatibullahrahel25@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
</p>

---

I design and ship **AI systems with real architectural decisions behind them** — structured generation, multi-phase completions, scoring engines, re-scoring infrastructure, and cost-aware LLM usage. My background is full-stack TypeScript + MERN; my current focus is production AI engineering: how systems fail, how they scale, and how to make them explainable.

Currently deepening: **LangChain.js · Mastra · LangGraph · Evals & Observability**

---

## 🔖 Featured Project

### AICA — AI Career Guidance Platform

> Replaces generic career counseling with a **data-driven, explainable recommendation system** built on a custom scoring engine, two-phase LLM completion, and a full re-scoring infrastructure.

**The System**

Users complete a 9-dimension behavioral assessment (strengths, learning style, collaboration preference, work style, career values). Each submission is scored against **200+ curated career pathways** using a custom **weighted matching engine** with four band multipliers — strong, supporting, weak, and penalty — producing normalized, comparable scores across both single-select and multi-select dimensions.

Recommendations are returned across a **3-layer hierarchy** (domain → field → individual pathway), each with a match percentage, dimension-level score breakdown, and an on-demand AI-generated explanation. Explanations are **cached after the first generation** — no redundant LLM calls on repeat views.

**Re-Scoring Infrastructure**

A dedicated re-scoring pipeline handles four trigger types: user assessment updates, pathway profile changes, algorithm version bumps, and manual admin actions. Runs as sequential batch processing with full audit output on every execution — the system is always in a known, traceable state.

**Roadmap Generation**

After pathway selection, Claude generates a phased action roadmap using **strict JSON schema enforcement**: steps nested inside phases, estimated hours (not vague day counts), and mandatory search queries on every resource reference — specifically to eliminate hallucinated URLs. Phase count is driven by the user's selected timeline tier.

**Two-Phase AI Advisor**

The embedded AI advisor runs on a two-phase completion architecture:

- **Phase 1** — silent, non-streaming 200-token call that detects whether web search is needed
- **Phase 2** — if search is triggered, Tavily fires and injects grounded results; streaming begins immediately after with full web context already loaded

The user sees search happening, then text flows — no generation delay after search completes.

**Architecture Decisions**

- TypeScript monorepo with **shared Zod schemas as the single source of truth** — assessment schema changes propagate automatically through models, validators, scoring logic, and API response types
- **Locale-independent scoring engine** — multilingual support (EN/FA/PS) handled via translation Maps embedded in MongoDB documents, resolved at query time with locale fallback; business logic never touches locale
- Three advisor modes: Deep, Focus, Guided — each with different context budget and tool access

**Stack:** TypeScript · Node.js · Express.js · Next.js · React · MongoDB · Mongoose · Anthropic Claude API · Tavily Search API · HuggingFace Inference API · Zod · REST API Design · Monorepo Architecture

🔗 [`rahel-swe/aica`](https://github.com/rahel-swe/aica)

---

## 🗂️ Other Projects

### Latoon — Social Platform Monorepo

Full-stack social platform built as a monorepo workspace — engineered and project-managed end to end. Includes a Next.js 16 client, Bun + Express API, shared type contracts, and a reusable UI package. Covers auth, session management, feed, posts, comments, reactions, i18n, and scalable backend layering.

**Stack:** Next.js 16 · React 19 · Bun · Express · MongoDB · Better Auth · TanStack Query · Zod · TypeScript · next-intl

---

### Cyber-Trust MS — Business Management Dashboard

Role-based internal dashboard for managing employees, projects, tasks, costs, and quotations. Built with clean client/server separation, JWT auth with token refresh, and seeded dev data for fast local setup.

**Stack:** React · Chakra UI · Bun · Express · MongoDB · Zustand · React Query · TypeScript

---

## 🛠️ Stack

**AI & LLM**
`Anthropic Claude API` `OpenAI API` `HuggingFace Inference` `Tavily` `Vercel AI SDK` `Prompt Engineering` `Streaming Completions` `Structured JSON Generation` `RAG`

**Languages & Runtime**
`TypeScript` `JavaScript (ES6+)` `Node.js` `Bun`

**Frontend**
`React` `Next.js` `React Native` `Tailwind CSS` `TanStack Query` `Zustand`

**Backend & Data**
`Express.js` `REST API Design` `MongoDB` `Mongoose` `PostgreSQL` `Prisma` `Zod`

**Architecture**
`Monorepo Architecture` `Clean Architecture` `Scoring Engine Design` `Re-Scoring Infrastructure` `i18n Architecture`

**Tooling**
`Git` `Docker` `Vercel` `Vitest` `React Testing Library` `MSW`

---

## 📈 Currently

- Shipping AI features in production (chat, text generation, structured generation, search-augmented completions)
- Studying: LangChain.js · Mastra · LangGraph · multi-agent orchestration · evals
- Goal: AI Engineering Lead — own architecture and system design, not just implementation

---

<p align="center">
  <a href="https://www.linkedin.com/in/khatibullahrahel">LinkedIn</a> ·
  <a href="https://rahel-portfolio-one.vercel.app">Portfolio</a> ·
  <a href="mailto:khatibullahrahel25@gmail.com">khatibullahrahel25@gmail.com</a>
</p>
