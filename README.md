# ChatGPT User Review Sentiment Prediction 🚀

A Python-based toolkit to classify user reviews using OpenAI's GPT (or GPT-3.5/4) and/or traditional ML for sentiment analysis, topic extraction, and visualization insights.

## 🔍 Project Overview

This project processes user reviews (e.g., from Amazon, App Store, or other platforms), runs sentiment analysis, extracts key themes/topics, and generates actionable insights to identify strengths, weaknesses, and improvement suggestions.

Inspired by similar sentiment-analysis pipelines using GPT and classic NLP models ([Reddit][1], [GitHub][2]).

---

## ⚙️ Features

* **Review ingestion**: Load reviews from CSV or API.
* **Sentiment Classification**:

  * Via OpenAI GPT 3.5/4 using prompt engineering.
  * Alternatively, traditional ML (e.g. VADER, TextBlob, scikit-based classifiers).
* **Topic Extraction**:

  * Extract common phrases or topics from positive/negative reviews ([GitHub][2], [arXiv][3], [AmanXai][4]).
* **Improvement Suggestions**:

  * Aggregate sentiments and generate top‑N improvement recommendations.
* **Visualizations**:

  * Bar charts, word clouds, and sentiment trend plots.
* **Interactive App**:

  * Explore results via Jupyter or a Streamlit dashboard ([GitHub][5]).

---

## 🧰 Technologies

* **Python** 3.8+
* **Data handling**: `pandas`, `numpy`
* **NLP & Sentiment**: `NLTK`, `TextBlob`, `VADER`, `scikit-learn`
* **OpenAI API**: `openai`
* **Visuals**: `matplotlib`, `seaborn`, `wordcloud`, `plotly`
* **App (Optional)**: `streamlit`

---

## 📂 Project Structure

```
├── data/
│   └── reviews.csv              # Raw input reviews
├── notebooks/                   # Jupyter notebooks (analysis & prototyping)
│   └── sentiment_analysis.ipynb
├── src/
│   ├── data_loader.py           # Load and preprocess data
│   ├── sentiment.py            # Sentiment logic (GPT/traditional)
│   ├── topic_extraction.py      # Identify key themes/phrases
│   ├── suggest_improvements.py  # Generate improvement recommendations
│   └── visualize.py            # Plot and chart functions
├── app.py                       # Streamlit dashboard (optional)
├── run_pipeline.py             # End-to-end execution script
├── requirements.txt            # Python package requirements
└── README.md                   # This documentation
```

---

## 🚀 Setup & Quick Start

1. **Clone the repo**

   ```bash
   git clone https://github.com/Lokesh-kukudala/chatgpt-user-review-sentiment-prediction.git
   cd chatgpt-user-review-sentiment-prediction
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **(Optional) Set up OpenAI key**

   ```bash
   export OPENAI_API_KEY="your_api_key_here"
   ```

4. **Run the pipeline** (using GPT or fallback ML)

   ```bash
   python run_pipeline.py --input data/reviews.csv --model gpt
   ```

5. **Launch the Streamlit app**

   ```bash
   streamlit run app.py
   ```

   Browse to `http://localhost:8501` to explore.

---

## 🧪 Example Workflow

* **Load reviews** (CSV with `review` column)
* **Preprocess text**: lowercase → clean → tokenize
* **Choose sentiment engine**:

  * **GPT** – prompt-based classification (`Positive`, `Negative`, `Neutral`)
  * **Traditional** – e.g., VADER (`sia`), TextBlob, or scikit-trained model
* **Extract topics/phrases** with n-grams or GPT summarization
* **Generate prioritized improvement suggestions**
* **Visualize results**: sentiment distribution, word clouds, topic frequency, NPS scoring

---

## 🎯 Customization

You can customize:

* Sentiment thresholds and classification logic
* GPT prompts for domain-specific accuracy
* Topic extraction depth (ngrams, embeddings, clustering)
* Visualization style and metrics

---

## 🧠 Related Work & Inspiration

* GPT‑powered review analysis tutorials ([Reddit][6], [GitHub][5], [Read Medium articles with AI][7], [GitHub][2], [Medium][8], [AmanXai][4], [Medium][9])
* Combined use of GPT + embeddings for topic clustering ([Gist][10], [AmanXai][4])
* Traditional pipelines using ML (Logistic Regression, SVM, XGBoost) with visual analytics ([GitHub][2], [GitHub][11])

---




[1]: https://www.reddit.com/r/ChatGPT/comments/10qzrb0?utm_source=chatgpt.com "Cool side project using GPT-3 to analyze product reviews and measure customer satisfaction!"
[2]: https://github.com/Gunalan183/chatgpt_sentiment_analysis?utm_source=chatgpt.com "GitHub - Gunalan183/chatgpt_sentiment_analysis"
[3]: https://arxiv.org/abs/2307.10234?utm_source=chatgpt.com "SentimentGPT: Exploiting GPT for Advanced Sentiment Analysis and its Departure from Current Machine Learning"
[4]: https://thecleverprogrammer.com/2024/08/26/chatgpt-reviews-analysis-with-python/?utm_source=chatgpt.com "ChatGPT Reviews Analysis with Python | Aman Kharwal"
[5]: https://github.com/NandiniBehera/ChatGPT-Review-Analysis?utm_source=chatgpt.com "GitHub - NandiniBehera/ChatGPT-Review-Analysis: This project analyses ChatGPT user reviews to classify them as Positive, Negative, or Neutral using Sentiment Analysis. I have extracted common phrases, visualised trends, and identify areas for improvement, helping enhance user experience with data-driven insights"
[6]: https://www.reddit.com/r/ChatGPT/comments/125jc3a?utm_source=chatgpt.com "Create Stock Sentiment Analysis in Python using chatGPT | Adnan's Random bytes"
[7]: https://readmedium.com/sentiment-analysis-with-chatgpt-openai-and-python-use-chatgpt-to-build-a-sentiment-analysis-ai-2b89158a37f6?utm_source=chatgpt.com "Sentiment Analysis with ChatGPT, OpenAI and Python — Use ChatGPT to build a sentiment analysis AI…"
[8]: https://medium.com/%40sdmuhsin3011/beginners-guide-to-decoding-chatgpt-s-popularity-discover-user-insights-with-python-be3f6f9754e8?utm_source=chatgpt.com "What are people saying about ChatGPT? Sentiment Analysis for Beginners | by Sdmuhsin | Medium"
[9]: https://medium.com/design-bootcamp/how-i-used-chatgpt-to-perform-user-review-analysis-from-appstore-6bc9266c428a?utm_source=chatgpt.com "How I used ChatGPT to perform user review analysis from appstore! | by Shiv Viswanathan | Bootcamp | Medium"
[10]: https://gist.github.com/taube-ms/d2653fc97dffd2e223f0fc8b495d2fee?utm_source=chatgpt.com "Customers reviews analyzer app using AI · GitHub"
[11]: https://github.com/SaloniJhalani/ChatGPT-Reviews-Sentiment-Analysis?utm_source=chatgpt.com "GitHub - SaloniJhalani/ChatGPT-Reviews-Sentiment-Analysis: This project focuses on performing sentiment analysis on ChatGPT reviews obtained from the App Store."
