# Enron-Email-Dataset
# Unsupervised Learning Analysis of the Enron Email Corpus

## Overview
This project performs an unsupervised learning analysis on the Enron email corpus. The analysis includes data preprocessing, clustering, PCA, TF-IDF analysis, sentiment analysis, and topic modeling.

## Dataset
Download the Enron email dataset from [CMU Enron Corpus](https://www.cs.cmu.edu/~enron/). The dataset is provided as a compressed file named `enron_mail_20150507.tar`. After extraction, the emails are stored in the `maildir` folder.

## Workflow
### 1. Data Preprocessing
#### **Step 1: Initial Data Cleaning**
- Run `Datapreprocessing1.ipynb`.
- This script extracts four key columns: `subject`, `sender`, `recipients`, and `body`.
- Saves the output as `emails.csv`.

#### **Step 2: Further Cleaning**
- Run `Datapreprocessing2.ipynb`.
- Loads `emails.csv` and removes duplicate values.
- Converts all words to lowercase.
- Identifies and visualizes the **Top 10 senders** and **Top 10 recipients**.
- Saves the cleaned dataset as `df_cleaned.csv`.

### 2. Clustering & PCA
- Run `Cluster.ipynb`.
- Inputs `emails.csv` to perform clustering and PCA.
- Saves the clustering results as CSV files in the `PCA` folder.

### 3. TF-IDF Analysis
- Run `TFIDF.ipynb`.
- Uses `stopwords-en.txt` and files in the `output` folder (`cut_words.json`, `word_idf.json`).
- Computes Term Frequency-Inverse Document Frequency (TF-IDF) for email texts.
- Saves the results as `keywords_tfidf.csv`.

### 4. Sentiment Analysis
- Run `Sentiment_Analysis.ipynb`.
- Performs sentiment analysis on the email corpus.

### 5. Topic Modeling (LDA)
- Run `Topic_modeling.ipynb`.
- Performs Latent Dirichlet Allocation (LDA) for topic modeling.

## Output Files
- `emails.csv`: Extracted email data with relevant columns.
- `df_cleaned.csv`: Preprocessed dataset.
- `PCA/`: Folder containing clustering and PCA results.
- `keywords_tfidf.csv`: TF-IDF keyword results.
- Additional outputs from sentiment analysis and topic modeling.

## Requirements
Ensure the following Python libraries are installed:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn nltk gensim
```

## Running the Analysis
Execute each Jupyter Notebook in the order specified above to complete the analysis.

## Acknowledgment
The Enron email dataset is publicly available from Carnegie Mellon University.

---
This README provides step-by-step instructions to conduct an unsupervised learning analysis on the Enron email corpus.
