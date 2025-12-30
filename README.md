# House of STR Insights

Turn short-term rental reviews into AI-driven retrospectives with exact upgrade recommendations, purchase links, and revenue-lift ROI scoring - works across any PMS with a single config change.

![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey)

## Table of Contents

1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Feature Matrix](#feature-matrix)
4. [How It Works](#how-it-works)
5. [Example Output](#example-output)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Roadmap](#roadmap)
9. [Contributing](#contributing)
10. [License](#license)

## Overview

House of STR Insights converts guest reviews from Airbnb & Vrbo (sourced **legally via PMS API integrations**) into structured intelligence using OpenAI.

It delivers:

- sentiment analysis
- operational & aesthetic issues
- exact upgrade suggestions
- ROI revenue-lift impact scores
- and product purchase links or similar alternatives

No scraping. Just compliant STR insights at scale.

## Key Features

- **Universal PMS Adapter** → Change provider in one line:

` PMS_PROVIDER = "Guesty"  # Guesty, Hostaway, Lodgify, Hostfully, Hospitable, iGMS `
- OpenAI-powered review analysis
- Extracts **exact upgrades** with product examples + links
- ROI scoring focused on **revenue lift**
- Portfolio-level ROI ranking
- Dashboard-ready JSON output
- Cost-efficient, minimal dependencies

## Feature Matrix
| Capability | Description |
--- | --- |
| PMS Adapter Pattern |	Plug-and-play support for multiple PMS providers |
| OpenAI Sentiment | Classifies tone & satisfaction signals |
| Upgrade Extractor |	Identifies real improvement opportunities (coffee bar, lighting, shower doors, etc.) |
| Purchase Link Finder | Provides real or close alternative product links |
| ROI Impact Score | Rates revenue-lift potential per upgrade (1–10) |
| Retrospective Summary	| 2-sentence host-focused recap |
| Portfolio Ranking	| Top 5 ROI upgrades across all listings |
| Output Format	| Console JSON, ready for dashboards, BI, or automation |

## How It Works
1. Pull reviews from selected PMS API
2. Group reviews by property/listing
3. Send reviews to OpenAI for analysis
4. Extract:
  - sentiment score & label
  - operational issues
  - aesthetic suggestions
  - upgrade ideas + purchase links
  - ROI impact score
5. Generate retrospective summary
6. Rank top portfolio upgrades
7. Print JSON to console

## Example Output
```json
{
  "avg_rating": 4.83,
  "sentiment_label": "Positive",
  "upgrades": [
    {
      "item": "Modern sliding shower door",
      "category": "Aesthetic",
      "reason": "Guests mention outdated bathroom feel",
      "purchase_link": "EXAMPLE_SHOWER_DOOR_LINK",
      "roi_impact": 8
    },
    {
      "item": "Dedicated coffee bar station",
      "category": "Operational",
      "reason": "Guests love coffee but request better setup",
      "purchase_link": "EXAMPLE_IKEA_COFFEE_BAR_LINK",
      "roi_impact": 7
    }
  ],
  "ai_summary": "Guests are highly satisfied but bathroom aesthetics and coffee experience present revenue-boosting opportunities. Prioritize modern bathroom upgrades and a curated coffee station to increase nightly rate and conversion appeal."
}
```

## Installation
`` pip install requests openai ``

## Usage
`` python str_review_analyzer.py ``

## Roadmap
- Review embeddings for clustering
- Automated upgrade alerts (Slack/Discord)
- Review-driven UGC generator
- ROI impact simulation on pricing
- STR investment scorecards

## Contributing
We welcome contributions!

### How to contribute:
1. Fork the repo
2. Create a new branch: `feature/your-idea`
3. Commit your changes
4. Push and open a Pull Request

Ideas we’re excited about:
- New PMS adapters
- Smarter ROI scoring models
- Additional upgrade categories
- UI dashboards
- Automation hooks

## License

MIT License - free to use, modify, and scale.
