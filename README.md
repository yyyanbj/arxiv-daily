# 📚 arxiv-daily

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=for-the-badge&logo=python)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/yyyanbj/arxiv-daily?style=for-the-badge&logo=github)](https://github.com/yyyanbj/arxiv-daily/stargazers)
[![Auto Update](https://img.shields.io/badge/Auto_Update-Daily-brightgreen?style=for-the-badge&logo=github-actions)](https://github.com/yyyanbj/arxiv-daily/actions)

> Automated daily arXiv paper curation — tracking latest research across AI, Robotics, and Machine Learning topics.

📅 **Automated deployment**: Daily at 10:28:42 Asia/Shanghai

<!-- TOC -->
- [About](#-about)
- [Features](#-features)
- [How It Works](#-how-it-works)
- [Add Your Topics](#-add-your-topics)
- [Database](#-database)
- [Contributing](#-contributing)

---

## 🔍 About

This project automatically scrapes and organizes papers from [arXiv](https://arxiv.org/) based on predefined keywords and topics. It's perfect for researchers and developers who want to stay updated with the latest developments in AI and robotics without manually searching every day.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Daily Updates** | Automated daily scraping via GitHub Actions |
| **Multi-Topic Tracking** | Covers Robot & Agent, Vision-Language Models, Imitation Learning, etc. |
| **Structured Format** | Papers organized by topic with metadata (date, title, authors, links) |
| **PDF & Code Links** | Direct links to papers and associated code repositories |
| **Customizable** | Add your own keywords in `topic.yml` |

---

## ⚙️ How It Works

```
GitHub Actions (daily schedule)
    ↓
Scrape arXiv by Keywords
    ↓
Extract Paper Metadata
    ↓
Link to PDFs & Code
    ↓
Update Database
```

---

## 📝 Add Your Topics

Want to track different research topics? It's easy!

### Step 1: Edit `topic.yml`

Open [`database/topic.yml`](database/topic.yml) and add your keywords:

```yaml
topics:
  - name: "Your Topic Name"
    keywords:
      - "keyword1"
      - "keyword2"
      - "multi word phrase"
```

### Step 2: Submit a PR

Fork this repo, make your changes, and submit a pull request. Your topics will be included in the next deployment.

---

## 🗄️ Database

### Storage Structure

```
database/
├── topic.yml          # Your topic/keyword definitions
└── storage/           # Historical paper records
    ├── 2026-04-05/    # Daily snapshots
    ├── 2026-04-04/
    └── ...
```

### Paper Entry Format

Each paper entry includes:

| Field | Description |
|-------|-------------|
| **Publish Date** | Date on arXiv |
| **Title** | Paper title |
| **Authors** | Author list |
| **PDF** | Link to arXiv PDF |
| **Code** | Link to GitHub repository (if available) |

---

## 🤝 Contributing

We welcome contributions! Here's how to help:

1. **Add Topics** — Edit `topic.yml` with new research keywords
2. **Fix Links** — Help update broken paper/code links
3. **Improve Structure** — Suggestions for better organization

### Quick Start

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/arxiv-daily.git

# Install dependencies
pip install -r requirements.txt

# Run locally
python scrape.py
```

---

## 📚 Resources

- [arXiv](https://arxiv.org/) — Open access to 2M+ research papers
- [arXiv API](https://info.arxiv.org/help/api/basics.html) — Programmatic access

---

*README optimized with [Gingiris README Generator](https://gingiris.github.io/github-readme-generator/)*
