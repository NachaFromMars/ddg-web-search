# ddg-web-search — Keyless web search via DuckDuckGo Lite

> Search the web without any API key, using DuckDuckGo Lite through web_fetch. The dependable fallback when your primary search provider isn't configured.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
ddg-web-search performs web searches with no API key by querying DuckDuckGo Lite through the built-in `web_fetch` tool. It uses a simple URL pattern with URL-encoded queries, extracts results as text, and supports regional filtering. Use it as a primary search method when no API key is available, or as a fallback when `web_search` returns a `missing_brave_api_key` error. Follow with `web_fetch` on selected URLs to get full page content.

## Features
- **Zero dependencies** — just `web_fetch`, no installs, no API key
- **Region filter** — `&kl=us-en`, `au-en`, `uk-en`, `de-de`, `fr-fr`, and more
- **Search-then-fetch** — search DDG → pick best URLs → `web_fetch` full content
- **Ad filtering** — skip "Sponsored link" entries in results

## Usage / Quick Start
```
web_fetch(
  url="https://lite.duckduckgo.com/lite/?q=your+query+here&kl=us-en",
  extractMode="text",
  maxChars=8000
)
```
URL-encode the query (spaces as `+`). Results come as numbered title/snippet/URL entries.

## Trigger Keywords (OpenClaw)
search fallback, no API key, DuckDuckGo search, web search without key, missing_brave_api_key

## Related Skills
- [duckduckgo-search](https://github.com/NachaFromMars/duckduckgo-search) — Python library alternative
- [deep-research-pro](https://github.com/NachaFromMars/deep-research-pro) — multi-source research using DDG

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
