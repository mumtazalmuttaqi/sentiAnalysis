# 📊 Olist E-Commerce Analytics Dashboard  
**Power BI Visualization with Python + LeIA Sentiment Analysis**

This dashboard visualizes sales performance, order behavior, and customer sentiment using the Olist Brazilian E-Commerce Public Dataset. The project integrates Python inside Power BI, utilizing **LeIA**, a lexicon-based sentiment analysis library designed specifically for the Portuguese language—making sentiment results more accurate for Olist reviews.

---

## 🚀 Key Features

### **1. KPI Cards**
- Total Payment  
- Total Orders  
- Total Sentiment Comments  

---

## 📈 Monthly Trends

### **Order & Payment Trend Comparison**
A combined bar and line chart visualizing:
- Monthly order volume  
- Total payment (R$)  
- Relationship between orders and revenue  

### **Monthly Sentiment Trend**  
Tracks the number of sentiment-labeled comments per month.

---

## 🧠 Sentiment Analysis Using Python + LeIA

The sentiment engine uses the **LeIA** library (Léxico para Inferência Adaptada), specialized for **Brazilian Portuguese**, making it ideal for Olist customer reviews.

### **Python Tasks:**
1. Text preprocessing  
2. Sentiment scoring using LeIA  
3. Generating positive & negative wordclouds  

### **Python Libraries Used**
```python
pandas
nltk
leIA
matplotlib
```

### Example Code
```python
from leIA.leia import SentimentIntensityAnalyzer

sia = SentimentIntensityAnalyzer()
score = sia.polarity_scores(text)

sentiment = "positive" if score["compound"] >= 0 else "negative"
```

---

## 🔄 Sentiment Visuals

### **Sentiment Proportion**
Donut chart showing:
- Positive reviews  
- Negative reviews  

### **Wordclouds**
- Frequent positive keywords  
- Frequent negative keywords  

---

## 📦 Sentiment by Product Category
Visual comparison of positive vs negative sentiment for each product category.

---

## 💰 Total Payment by Category
Ranking of product categories based on revenue contribution.

---

## 📁 Repository Structure
```
/Olist-Ecommerce-Dashboard/
│
├── README.md
├── dashboard.pbix
├── /images/
│   └── dashboard_preview.png
├── /python/
│   ├── preprocessing.py
│   ├── sentiment_leia.py
│   └── wordcloud_generator.py
└── /data/
    └── olist_processed.csv
```

---

<img width="1019" height="571" alt="Screenshot 2025-11-23 200935" src="https://github.com/user-attachments/assets/580d9f47-a080-4b45-a672-c44bc6ad9b7b" />

## 💡 Insights
- Over **80%** customer reviews are positive (LeIA-based result)  
- Health Beauty & Watches Gifts have the highest positive sentiment  
- Negative reviews often relate to late delivery & packaging  
- Revenue rises significantly mid–year  

---

## 🛠️ How to Use the Dashboard

1. Clone this repository  
2. Open `dashboard.pbix` in Power BI Desktop  
3. Install required Python libraries:
   ```bash
   pip install leIA nltk wordcloud matplotlib pandas
   ```
4. Set Python path in **Power BI → Options → Python scripting**  
5. Refresh report to process sentiment analysis  

---



