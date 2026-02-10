# AI Agent Automation (n8n) — Trend Discovery + Content Generation

Automation workflows built with **n8n + Google Gemini** to collect e-commerce + news signals,
detect trends, and generate marketing insights/content (prototype focused on the rugs/home decor space).

> Disclaimer: Personal/externship project work. Not affiliated with or endorsed by Wayfair.

## What’s included (workflows)

### 1) Consumer Trend Discovery AI Agent
Chat-triggered workflow that:
- Classifies whether the user’s request is about “rug trends”
- Collects signals from RSS feeds + search + e-commerce links
- Filters recency (e.g., last ~7 days) and produces a summarized output using Gemini

File: `workflows/01_trend_discovery_agent.json`

### 2) Amazon Scraper (v1)
Scrapes Amazon product pages and extracts:
- title, price, bullet details, pattern/variant text (where available)

File: `workflows/02_amazon_scraper_v1.json`

### 3) Amazon Scraper (v2 — Nov 20 build)
Improved wiring/version for handling Amazon URLs and scrape batches.

File: `workflows/03_amazon_scraper_v2_2024-11-20.json`

### 4) AI-Generated Insights & Content Automation (Project 4)
Given Amazon/Walmart product or collection URLs:
- Scrapes product signals
- Generates **trend / competitor / style** signals
- Produces **marketing insights + HTML content output** using Gemini

File: `workflows/04_insights_content_automation_project4.json`

## How to use
1. Open your n8n instance
2. Import a workflow JSON: **Workflow → Import from file**
3. Configure credentials in n8n (Gemini / HTTP / etc.)
4. Run a manual test execution, then enable triggers/schedules as needed

## Security notes
- Do NOT commit API keys to GitHub.
- Replace any hardcoded keys with environment variables or n8n credential entries.
- If a key was committed, rotate it immediately.

## Repo structure
- `workflows/` — n8n exported workflow JSON files
- `docs/` — setup notes / environment variables
- `assets/` — screenshots (workflow canvas, sample outputs)
