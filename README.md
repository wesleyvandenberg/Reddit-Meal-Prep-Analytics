# 🧠 Reddit Community Analytics — r/MealPrepSunday

**Technologies:** Python · PRAW (Reddit API) · pandas · matplotlib · nltk · TextBlob · WordCloud  
**Skills Demonstrated:** Data Collection (APIs) · Data Cleaning & Modeling · NLP · Sentiment Analysis · Visualization · Automation & Reproducibility

---

## 📘 Project Overview

This project builds a full end-to-end analytics pipeline for **r/MealPrepSunday**, one of Reddit’s largest communities centered on meal prepping and healthy eating.  
The goal was to **quantify community engagement**, extract **key discussion topics**, and analyze **sentiment trends** across thousands of user posts and comments.

The notebook automates:

1. **Data ingestion** from Reddit via API (PRAW)
2. **Data normalization and cleaning** into structured tables
3. **Natural Language Processing (NLP)** on text data
4. **Sentiment analysis** and engagement ranking
5. **Visual storytelling** through plots and word clouds

Beyond exploration, the pipeline is designed for **reproducibility, fault tolerance**, and **scalable data enrichment**, resembling the foundation of a lightweight social-listening system.

---

## 🚀 Key Achievements

### 1. Automated Data Collection (Reddit API)

- Built a **custom RedditCollector** class to gather up to **1,000 top posts** and **all top-level comments** from `r/MealPrepSunday`.
- Implemented **checkpointing**, **progress bars**, and **CSV persistence** to handle API rate limits and restarts gracefully.
- Normalized outputs into **submissions**, **comments**, and **authors** datasets for relational querying.

### 2. Data Cleaning & Structuring

- Parsed and transformed JSON response data into **structured pandas DataFrames**.
- Converted timestamps to datetime objects, removed nulls and duplicates.
- Exported normalized tables to CSV for reuse across projects or dashboards.

### 3. Natural Language Processing (NLP)

- Preprocessed text using `nltk`: lowercasing, stopword removal, punctuation stripping, and optional stemming.
- Calculated **term frequencies** for both posts and comments, revealing trending ingredients, recipes, and health terms.

### 4. Engagement & Influence Metrics

- Defined **influence** as total comment count per post to surface the most discussion-generating topics.
- Identified top contributors and engagement outliers — enabling community and content insights.

### 5. Sentiment Analysis

- Performed **comment-level sentiment scoring** using `TextBlob` to assess positivity, negativity, and subjectivity.
- Visualized polarity distributions and extracted **most positive** and **most negative** comment examples.
- Produced interpretable insights into how tone shifts across posts and themes.

### 6. Visualization & Reporting

- Used `matplotlib` for cumulative submission trends and comment frequency analysis.
- Generated **word clouds** for submission titles and top-ranked discussions.
- Combined visuals and metrics into a coherent narrative suitable for executive reporting or stakeholder presentations.

---

## 🧩 Folder Structure

```
project_v2/
│
├── data/
│   ├── mealprepsunday_reddit_submission.csv
│   ├── mealprepsunday_reddit_comments.csv
│   ├── mealprepsunday_reddit_authors.csv
│
├── project_v2.ipynb
│
└── README.md
```

---

## 💡 Technical Highlights

| Component              | Libraries                 | Description                                  |
| ---------------------- | ------------------------- | -------------------------------------------- |
| **API Integration**    | `praw`                    | Custom Reddit API wrapper with checkpointing |
| **Data Wrangling**     | `pandas`, `numpy`         | Normalization, grouping, timestamp parsing   |
| **Text Processing**    | `nltk`                    | Tokenization, stopword filtering             |
| **Sentiment Analysis** | `textblob`                | Polarity & subjectivity scoring              |
| **Visualization**      | `matplotlib`, `wordcloud` | Temporal trends & lexical visualization      |

---

## 📊 Example Outputs

- 📈 **Cumulative post activity chart** — shows long-term subreddit growth
- ☁️ **Word clouds** — visualize popular meal terms (“chicken,” “prep,” “budget,” “protein”)
- 💬 **Sentiment histograms** — distribution of positive vs. negative comments
- 🧮 **Top 10 most influential posts** — sorted by comment volume

---

## 🧠 Analytical Insights

- The subreddit’s engagement spikes cyclically, aligning with **weekends** (Sunday meal prep theme).
- Most discussions center on **high-protein** and **budget-friendly** meal prep, reflecting user priorities.
- Sentiment analysis shows a **net-positive community tone**, with outliers around dietary debates or time-management struggles.
- Influential threads tend to combine **visual appeal (images)** with **utility (prep guides, shopping lists)**.

---

## 🧩 Skills Demonstrated to Employers

- **Full-stack data analytics:** Designed an end-to-end system from data collection to insight visualization.
- **API engineering & automation:** Implemented checkpointed API calls, making the system restart-safe.
- **NLP expertise:** Cleaned, tokenized, and modeled text at scale for interpretability.
- **Analytical storytelling:** Translated raw Reddit text into business-style insights and visuals.
- **Scalable data practices:** Structured the project to extend easily to other subreddits or social datasets.

---

## 🔍 Future Extensions

- **Topic modeling (LDA / BERTopic):** Uncover latent themes across discussions.
- **Network analysis:** Map interactions between authors and comment chains.
- **Advanced sentiment models:** Replace TextBlob with transformer-based models (e.g., RoBERTa, VADER).
- **Dashboard deployment:** Create a Streamlit or Plotly Dash app for interactive community analytics.
- **Ethics & privacy:** Integrate configurable anonymization and PII filtering for safe sharing.

---

## 💬 Interview Talking Points

When discussing this project:

- Emphasize that it replicates **real-world social-listening analytics**, common in **marketing, risk, or policy analysis**.
- Mention your design decisions (checkpointing, normalization) as examples of **software-engineering maturity** in data science.
- Highlight interpretability: TextBlob’s polarity is **transparent and reproducible**, suitable for stakeholder contexts.
- Frame future improvements as **data-product thinking** — adding interactivity, scalability, and model upgrades.

---

## 🏁 Summary

> This project showcases the ability to transform unstructured social data into actionable insights through **robust data engineering, text analytics, and visualization**.  
> It reflects a complete analytical workflow — from raw API data to sentiment-driven storytelling — while adhering to principles of reproducibility, modularity, and clarity.
