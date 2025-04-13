# 🏢 LinkedIn Company Pages Scraper with Crawlbase

## 📝 Description

This repository provides a Python-based solution to scrape detailed public company information from LinkedIn using the [Crawlbase Crawling API](https://crawlbase.com/crawling-api-avoid-captchas-blocks).

It includes:

- A scraper that sends asynchronous requests to LinkedIn company page URLs.
- A retrieval script that fetches the structured company data using the request ID (RID).

📖 Read the full tutorial: [How to Scrape LinkedIn](https://crawlbase.com/blog/how-to-scrape-linkedin/)

## 🔧 Tools Used

- [`crawlbase`](https://pypi.org/project/crawlbase/) – for accessing Crawling and Storage APIs
- `json` – for handling structured output
- `Python 3.6+`

## 📦 Installation

Install the required package:

```bash
pip install crawlbase
```

## 🚀 Scraper: LinkedIn Company Page Scraper

**File:** `linkedin_company_scraper.py`

### ✅ What It Does

- Sends an asynchronous scraping request to a LinkedIn company page.
- Returns a rid (request ID) to be used for retrieving the full response.

### ⚙️ How to Run

1. Replace `YOUR_API_TOKEN` with your Crawlbase token.
2. Set the LinkedIn company page `URL`.

```bash
python linkedin_company_scraper.py
```

### 🧪 Sample Output

```json
{
	"rid": "f270321bbebe203b43cebedd"
}
```

## 📄 Retrieval: Get Company Data

**File:** `linkedin_company_retrieve.py`

### ✅ What It Does

- Retrieves and prints the stored company page data using the rid.

### ⚙️ How to Run

1. Replace YOUR_API_TOKEN and RID in the script.

```bash
python linkedin_company_retrieve.py
```

### 🧪 Sample Output

```json
{
  {
  "title": "Amazon",
  "headline": "Software Development",
  "cover_image": "https://media.licdn.com/dms/...",
  "company_image": "https://media.licdn.com/dms/...",
  "url": "https://www.linkedin.com/company/amazon",
  ...
}
```

## 📌 To-Do

- Support for scraping multiple company pages
- Export company data to CSV/JSON
- Add CLI options for input/output
- Implement retry and error-handling logic

## 💡 Why Scrape LinkedIn Company Pages?

- Research competitors and market trends
- Monitor public-facing company updates
- Build datasets for lead generation and analytics
