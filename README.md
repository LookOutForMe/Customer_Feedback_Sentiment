# 📊 Mini Project: Customer Feedback Sentiment Analysis

## 🏢 Industry
**Customer Experience**

## 🎯 Objective
The aim of this project is to analyze customer feedback from product reviews and perform sentiment analysis using Natural Language Processing (NLP) techniques. Insights are then stored in an SQL database and queried to understand customer sentiment trends and top complaints.

---

## 🧩 Project Overview

This project involves:
- Extracting and processing customer reviews and ratings from a CSV dataset.
- Performing sentiment analysis using Python NLP libraries such as **VADER**.
- Storing the sentiment results and associated metadata into an SQL database.
- Analyzing sentiment trends per product and identifying top complaints.

---

## 📁 Dataset Source

**Customer Reviews Dataset:**  
[Kaggle: Amazon Product Reviews](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews)

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** for data manipulation
- **NLTK / VADER** for sentiment analysis
- **SQLite** for database management
- **Matplotlib / WordCloud** for visualizations
- **Jupyter Notebook** for implementation and documentation

---

## ✅ Tasks Implemented

### Python Implementation
- Load and clean review text and rating data from CSV.
- Perform sentiment analysis using TextBlob/VADER.
- Assign sentiment scores to each review.
- Generate sentiment distribution plots and word clouds.
- Save processed results to SQL.

### SQL Implementation
- Create table `reviews(id, product_id, text, sentiment_score, rating)`.
- Insert cleaned and analyzed data into the database.
- Execute SQL queries to compute KPIs:
  - Average sentiment score per product.
  - Count of positive and negative reviews.
  - Extract top keywords from negative reviews.

---

## 📊 KPIs and Formulas

| KPI                      | Description / Formula                                 |
|--------------------------|--------------------------------------------------------|
| Positive Feedback Rate   | `Count(Positive Reviews) / Total Reviews`             |
| Negative Feedback Rate   | `Count(Negative Reviews) / Total Reviews`             |
| Average Sentiment Score  | `AVG(Sentiment Score)`                                |
| Top Complaints           | Most frequent keywords in negative reviews            |

---

## 🧮 SQL Schema

```sql
CREATE TABLE reviews (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    product_id TEXT,
    text TEXT,
    sentiment_score REAL,
    rating REAL
);

--------------------------------------------------------------------------------------------------

📌 Key Insights
Sentiment Distribution: Visualized to show the polarity and subjectivity of reviews.

Top Complaints: Extracted by analyzing word frequencies in negative sentiment reviews.

Product Comparison: Products are compared based on sentiment averages and feedback distribution.

📷 Visual Outputs
📉 Sentiment Score Distributions

https://drive.google.com/file/d/1WzYO2EO1sCyawoOmW_iVSvTVRxOJJlQ1/view?usp=sharing

☁️ Word Cloud for Negative Reviews

https://drive.google.com/file/d/15-dID_2IPssBq5Z18D6rrQnHruPZu2PJ/view?usp=sharing

🚀 How to Run
1. Clone this repository or download the .ipynb file.

2. Install required libraries using:

pip install pandas textblob nltk matplotlib wordcloud sqlite3

3. Run the Jupyter Notebook step by step.

4. Inspect results and visualizations generated.

👨‍💻 Author

Ariyan Shaw