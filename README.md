# Fake news detection 

## Overview

This project focuses on detecting **fake news** using **Natural Language Processing (NLP)**, **Machine Learning**, and **Topic Modeling** techniques. The goal is to build a classification model to identify whether a news article is real or fake and analyze the prevalent topics in fake news. The models are designed to be integrated into a **Chrome plugin** that provides real-time feedback to users about the veracity of the articles they read online.

---

## Key Objectives

- Develop classification models (**Logistic Regression** and **Naive Bayes**) to detect fake news.
- Use **Latent Dirichlet Allocation (LDA)** for topic modeling to uncover key topics in fake and real news articles.
- Implement the models in a Chrome plugin for real-time news verification.

---

## Key Questions

- Are fake news articles more frequent in certain categories?
- Are there specific topics that are more susceptible to fake news?
- Do the titles of fake news articles present recurring patterns?

---

## Text Preprocessing

The first step in the pipeline is **text preprocessing**, where both article titles and the content are cleaned to improve the performance of the classification models and topic modeling.

### Preprocessing Function

Implemented two preprocessing functions, **`preprocess_text`** and  **`preprocess_title`** to handle the following tasks:

1. **Expand contractions**: Convert contractions like "can't" to "cannot" for consistency.
2. **Remove noise**: Eliminate URLs, mentions (`@username`), and hashtags (`#topic`) from the text.
3. **Tokenization and Stopwords removal**: Split text into individual words and remove common words (stopwords) using **Gensim**.
4. **Lemmatization**: Reduce words to their base form using **POS tagging** (so verbs, adjectives, and other POS are handled).

---
## Models Used
### 1. **Latent Dirichlet Allocation (LDA)**
   - **Topic modeling** technique applied to uncover hidden topics within news articles.
   - Implemented using the **Gensim** library to understand common themes and subject areas present in both real and fake news.
     
### 2. **Logistic Regression**
   - Applied to classify news as either real or fake based on text patterns.
   - Uses **TF-IDF** (Term Frequency-Inverse Document Frequency) vectorization for feature extraction.

### 3. **Naive Bayes**
   - A simple probabilistic classifier effective for text classification tasks, such as fake news detection.
   - Uses the same **TF-IDF** vectorization for feature extraction.
