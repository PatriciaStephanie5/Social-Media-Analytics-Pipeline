# EchoTrend Analytics: The Latte Loyalty Gap

[![n8n](https://img.shields.io/badge/Automation-n8n-red?logo=n8n)](https://n8n.io)


**A simulated end-to-end social listening project that automates data enrichment and visualizes the competitive landscape between UrbanBrew Coffee and RoastLab.**


---

## Project Overview

**Business Context:**  
UrbanBrew Coffee, a national chain with 150 locations, wanted to understand why their high-volume social media presence wasn't translating into stronger brand sentiment compared to niche competitor RoastLab.

**The Challenge:**  
- UrbanBrew posts 3× more content than RoastLab
- RoastLab enjoys higher ratings and more engaged conversation
- Hypothesis: Promotional content dilutes genuine engagement

**The Solution:**  
This project simulates a complete data pipeline:
1. **Scrape** social media data (CSV simulation)
2. **Enrich** with sentiment, hashtag extraction, and business categories using **n8n**
3. **Visualize** insights in **Tableau** to tell a compelling story
4. **Recommend** actionable strategy shifts

---

## Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Data Simulation** | Python (Faker / Mockaroo) – simulated CSV |
| **Data Automation** | n8n Cloud (workflow orchestration) |
| **Data Enrichment** | JavaScript Code Nodes (text cleaning, sentiment lexicon, categorization) |
| **Visualization** | Tableau Public (interactive dashboards & story) |
| **Version Control** | Git & GitHub |

---

## Repository Contents

| Path | Description |
| :--- | :--- |
| `data/raw_social_feed_2026_Q2.csv` | Original simulated dataset (5 sample rows, expandable) |
| `data/enriched_social_data.csv` | Final dataset after n8n enrichment |
| `n8n/EchoTrend_Enrichment_Workflow.json` | Exported n8n workflow (importable to any n8n instance) |
| `tableau/EchoTrend_Latte_Loyalty_Gap.twbx` | Tableau packaged workbook (optional) |
| `images/` | Screenshots of dashboards and story points |

---

## n8n Workflow Automation

The n8n workflow performs the following steps **without external API dependencies**:

1. **Manual Trigger** – JSON input simulating a CSV import.
2. **Code Node (JavaScript)** – Text cleaning, hashtag extraction, and ad flagging.
3. **Code Node (JavaScript)** – Lexicon-based sentiment analysis (positive/negative/neutral).
4. **Code Node (JavaScript)** – Business categorization (Promotion / Service Issue / General).
5. **Spreadsheet File / Google Sheets** – Export enriched CSV.


---

## Tableau Story: The Latte Loyalty Gap

The Tableau story comprises **four key views**:

### 1. Executive Summary
- **KPI BANs**: Post volume and average sentiment by brand.
- **Insight**: UrbanBrew dominates volume but trails RoastLab in sentiment.

### 2. The Engagement Trap
- **Scatter Plot**: Likes vs. Comments, colored by brand and shaped by promotion flag.
- **Trend Lines**: Show divergent engagement patterns.
- **Finding**: Promotional posts (`#ad`) generate high likes but near‑zero conversation.

### 3. Vocabulary of Loyalty
- **Treemaps**: Most frequent words used in posts mentioning each brand.
- **Contrast**: UrbanBrew – *“giveaway”, “free”, “win”*  
  RoastLab – *“barista”, “farm”, “perfect”, “single origin”*

### 4. Strategic Recommendations
- Reduce promotional content from 35% → 15% of feed.
- Launch educational series (“Meet the Roaster”) with no sales links.
- Pilot “Express Pickup Lane” to address operational complaints.
- **Projected Impact**: +0.15 sentiment lift in 90 days.

**Explore the interactive story on Tableau Public:**  
[View Full Story](https://public.tableau.com/views/YourLink)

---

