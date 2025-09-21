# NLP-Disaster-Tweets
This project is part of a Kaggle competition called Natural Language Processing with Disaster Tweets. The goal is to predict whether a tweet is about a real disaster (1) or not (0).

# Project Structure

disaster-tweets-kaggle-mini-project.ipynb — main notebook with EDA, data cleaning, modeling, and results.

submission.csv — example prediction file submitted to Kaggle.

requirements.txt — dependencies to run the notebook.

# Steps Completed

## Problem and Data

Dataset from Kaggle competition: ~7,600 training tweets, ~3,200 test tweets.

Features: id, keyword, location, text. Target: target (0 or 1).

## Exploratory Data Analysis (EDA)

Checked missing values (many in keyword and location).

Target distribution is fairly balanced.

Tweets are short (~15 words on average).

Disaster tweets tend to be slightly longer.

## Modeling

Baseline: TF-IDF + Logistic Regression → Validation F1 ≈ 0.76

Sequential Model: BiLSTM with embeddings → Validation F1 ≈ 0.72

TF-IDF baseline outperformed BiLSTM, showing classical models can be strong on small datasets.

## Results and Analysis

TF-IDF worked best due to small dataset size and short tweets.

Neural model may improve with pretrained embeddings (GloVe/BERT) or more data.

## Conclusion

Best model was Logistic Regression with TF-IDF features.

Cleaning the text and limiting sequence length helped.

Future improvements: use pretrained embeddings, transformers, and add features like presence of URLs/hashtags.
