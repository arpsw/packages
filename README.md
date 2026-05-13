# ARP.software Composer Registry
===========================

This is a private [Composer](https://getcomposer.org/) registry for ARP.software modules, powered by [Satis](https://github.com/composer/satis).

Contains:
- `arpsw/core-module` — Foundation: shared Filament infrastructure, users, roles, permissions, media, tags, activity log
- `arpsw/ai-module` — AI agent system built on the neuron framework
- `arpsw/hrm-module` — Human Resource Management: employees, contracts, documents, competencies
- `arpsw/guidelines-skills` — Coding guidelines as AI skills for Laravel Boost

To use this, add to your `composer.json`:

```json
"repositories": [
    {
        "type": "composer",
        "url": "https://arpsw.github.io/packages/"
    }
]
```

Authentication is required to download the source packages. Run this once on your machine:

```bash
composer config --global github-oauth.github.com YOUR_GITHUB_TOKEN
```

This writes to `~/.composer/auth.json` and works automatically inside DDEV as well.

Head over to https://arpsw.github.io/packages/ to browse available packages.

**NOTE**: The actual registry is published to the [gh-pages](https://github.com/arpsw/packages/tree/gh-pages) branch via GitHub Actions on every push to `main`.
