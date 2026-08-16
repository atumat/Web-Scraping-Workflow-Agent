# 🕸️ Resilient Self-Healing Web Scraper

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Playwright](https://img.shields.io/badge/Playwright-Automation-green?logo=playwright)
![Pydantic](https://img.shields.io/badge/Pydantic-v2-red)
![License](https://img.shields.io/badge/License-MIT-purple)

> An autonomous web extraction engine that prevents pipeline breakage by dynamically repairing outdated or modified DOM selectors at runtime using LLM-assisted context parsing and strict Pydantic validation.

### 🌟 Key Features
- **Zero-Downtime Scraping:** Automatically detects `ElementNotFound` errors and queries an LLM to inspect the surrounding DOM tree and generate new, stable CSS/XPath selectors.
- **Adaptive Selector Caching:** Saves newly healed selectors to local/Redis storage, ensuring LLM calls are only made on failure ($O(1)$ lookup for subsequent runs).
- **Strict Data Contracts:** Powered by Pydantic models to guarantee clean, typed, and sanitized tabular data.
- **Headless Browser Execution:** Leverages Playwright for robust single-page application (SPA) and JavaScript rendering.
