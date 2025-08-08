# A Sentiment and Thematic Analysis of Canada's Digital Banking Landscape

## 1. Introduction & Business Objective
In the highly competitive Canadian digital banking sector, understanding public perception is crucial for strategic decision-making. This project was initiated to move beyond traditional metrics and tap into the authentic, unsolicited "voice of the customer."

**The primary business objective was to analyze public sentiment towards major Canadian digital-first financial brands on the social media platform Reddit.** The goal was to identify competitive strengths and weaknesses, quantify brand perception, and uncover the specific themes driving user frustration and satisfaction.

## 2. Data and Methodology
The analysis is based on a comprehensive **dataset of 31,668 public mentions** (posts and comments) collected from Reddit. The data was sourced from high-traffic Canadian finance subreddits (e.g., r/PersonalFinanceCanada) and brand-specific communities (e.g., r/Wealthsimple) over the last 12 months.

The project followed a multi-stage data science workflow:

**Data Acquisition:** A custom Python script using the PRAW library was developed to scrape all relevant data. This script included robust error handling to manage Reddit's API rate limits, ensuring a complete and unbiased data pull.<br>
 **Data Cleaning:** The raw text was meticulously cleaned and preprocessed using the Pandas library to prepare it for analysis. This involved removing duplicates, URLs, and special characters, and standardizing the text.<br>
**Sentiment Analysis:** We employed a pre-trained Natural Language Processing (NLP) model from Hugging Face (cardiffnlp/twitter-roberta-base-sentiment) to classify each of the 27,008 unique comments into Positive, Negative, or Neutral sentiment categories.<br>
**Thematic Analysis:** To gain deeper insights into the drivers of negative sentiment, we used a sophisticated Zero-Shot Classification model (facebook/bart-large-mnli) to categorize all 6,000+ negative comments into seven key business themes, such as 'Customer Service Issues' and 'Security & Fraud Concerns'.

## 3. Key Findings & Visualizations
The analysis produced several key outputs that quantify and visualize the public perception of each brand.

### A. Brand Performance Ranking
To create a fair comparison of brand sentiment, we calculated the "Positive Sentiment Share" – the percentage of all emotional comments (Positive or Negative) that are positive.

**Finding:** The ranking clearly shows **EQ Bank** as the market leader in customer satisfaction, as it is the only brand with a net positive sentiment score. **Koho** and **Neo Financial** rank at the bottom, indicating significant challenges with user perception.

### B. Comparative Pain Point Analysis
The thematic analysis provides the most strategic insight: a "Pain Point Profile" for each competitor. This chart shows what percentage of each brand's negative feedback is dedicated to a specific theme.

**Finding:** The data reveals a unique "fingerprint" of weaknesses for each brand. For example, **Koho's** negative sentiment is overwhelmingly driven by **Customer Service Issues (37%)**, while **EQ Bank's** primary pain point is **Security & Fraud Concerns (26%)**. This allows for a highly nuanced understanding of the competitive landscape.

## 4. Conclusion & Strategic Implications
The data tells a clear and consistent story. For the modern Canadian banking consumer, the fundamentals of trust, reliability, and support are paramount.

Across the entire market, the three biggest drivers of negative sentiment are **Security & Fraud Concerns (27%)**, **Account Access & Login (22%)**, and **Customer Service Issues (21%)**. Issues with specific app features or fees, while present, are secondary to these core pillars of the banking experience.

This project concludes that the brands that can deliver a secure, reliable, and well-supported service will have the most significant competitive advantage. The detailed thematic breakdown provides a strategic roadmap for identifying and targeting the specific operational weaknesses of key competitors.

## 5. Technologies Used
**Language:** Python

**Libraries:** Pandas, PRAW, Matplotlib, Seaborn, WordCloud

**NLP Models:** Hugging Face Transformers (cardiffnlp/twitter-roberta-base-sentiment, facebook/bart-large-mnli)

**Environment:** Jupyter Notebook
