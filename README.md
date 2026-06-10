# Sentiment Analysis on Social Media Data using Apache Spark

## 📖 Project Overview
This project focuses on **sentiment analysis of social media user reviews** using **Apache Spark** for large-scale data processing.  
We applied text preprocessing techniques, trained multiple machine learning models (Logistic Regression and Naïve Bayes), and compared their performance.  
Additionally, a simple **Streamlit-based UI** was created to visualize and interact with the results.

---

## 🎯 Objectives
- Handle and process **large-scale datasets** using Apache Spark  
- Perform **text preprocessing** (cleaning, tokenization, stopword removal, TF-IDF features)  
- Train and compare machine learning models for sentiment classification  
- Visualize results and comparisons  
- Build a **simple interactive UI** with Streamlit  

---

## 📂 Dataset
The project uses the **Yelp Open Dataset**, specifically the file:

```

yelp_academic_dataset_review.json

```

This dataset contains millions of user reviews, which are used for **sentiment classification (positive, negative, neutral)**.  
For access to the full dataset: [Yelp Dataset](https://www.yelp.com/dataset)

---

## ⚙️ Requirements
- Google Colab (or local Python 3.x environment)  
- Apache Spark  
- Python Libraries:  
  - `pyspark`  
  - `spark-nlp`  
  - `pandas`  
  - `matplotlib`  
  - `scikit-learn`  
  - `streamlit`  
  - `pyngrok`  

---

## 📁 Project Structure
```

Sentiment-Analysis-Spark/
│
├── sentiment_analysis_colab.ipynb   # Main Colab notebook
│
└── README.md

````

---

## 🚀 Running the Project on Google Colab
1. Install dependencies:
   ```python
   !pip install pyspark spark-nlp
````

2. Mount Google Drive:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. Load dataset:

   ```python
   data_path = "/content/drive/My Drive/Colab Notebooks/data/yelp_academic_dataset_review.json"
   ```

4. Preprocess the data:

   * Text cleaning
   * Tokenization
   * Stopword removal
   * TF-IDF feature extraction

5. Train machine learning models:

   * Logistic Regression
   * Naïve Bayes

6. Save and compare results:

   * Results are stored in `results/` as CSV files
   * Charts are saved in `charts/`

---

## 🖥️ Running the UI (Streamlit)

1. Install required packages:

   ```python
   !pip install streamlit pyngrok
   ```

2. Run the app with ngrok:

   ```python
   from pyngrok import ngrok
   public_url = ngrok.connect(8501, "http")
   print(f"🌐 Streamlit app link: {public_url}")

   !streamlit run app.py &
   ```

3. A temporary public link will be generated, e.g.:

   ```
   https://xxxx-xx-xx-xx.ngrok-free.app
   ```

⚠️ This link works **only while Colab is running**.

---

## 📊 Results & Analysis

* **Logistic Regression** outperformed Naïve Bayes on the Yelp dataset.
* Apache Spark significantly improved **scalability and processing speed** compared to non-distributed methods.
* Spark’s distributed approach makes the pipeline suitable for **large-scale, real-world sentiment analysis tasks**.

---

## 🔮 Future Work

* Deploy the Streamlit app permanently (Heroku, Streamlit Cloud, etc.)
* Experiment with deep learning models (BERT, Transformers)
* Extend to multilingual datasets
* Build interactive dashboards for advanced analysis

---

## Author

* **Yasaman Raoof Moghadam**
  MSc in Software Engineering
  *Big Data Sentiment Analysis with Apache Spark Project*

```

---
