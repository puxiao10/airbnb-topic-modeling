# Airbnb Review Topic Modeling – Seattle

This project analyzes customer reviews from Seattle Airbnb listings to uncover common themes using topic modeling. The goal is to help Airbnb hosts, investors, and researchers better understand what makes listings popular — and what guests value most — through both traditional and modern NLP techniques.

---

## 📊 Dataset

- **Source:** Seattle Airbnb Open Data  
- **File:** `data/sampled_reviews.csv`  
- **Details:** Contains 50,000 guest reviews with free-text comments, sampled from larger Airbnb review data.

---

## 🧠 Methods

- Text preprocessing (stopwords, stemming, cleaning)
- Exploratory Data Analysis (word frequency plots)
- Topic Modeling:
  - **TF-IDF + KMeans** for baseline clustering
  - **BERTopic** (BERT embeddings + HDBSCAN) for semantic-rich topic extraction
- Topic interpretation and visualization

---

## 🔍 Sample Visualizations

### Top Frequent Words After Cleaning

![Word Could](images/Topic_word_cloud.png)

---

## 🧩 Insights From Topic Modeling

The resulting topics were dominated by generic, high-frequency words like “great,” “location,” “place,” and “Seattle,” offering limited actionable insights. 
This revealed two key issues: 
	- the need for further preprocessing to remove common filler terms, and the 
	- limitations of TF-IDF in capturing nuanced or contextual language (e.g., “Space Needle view,” “quiet neighborhood”). 

### BERTopic Topic Distance Map

![Topic Distance Map](images/Topic_Distance_Map.png)

---

## 🧩 Insights From BERTopic

The resulting topics were much better now, we started to see useful information like “mattress”, “rooftop”, “pillow”, or location near “restaurant”, “alki beach”, etc.
From the distance map, we can see many topics are very close to each other, so we can merge them together for better summary.


