# kannada-pos-aware-extractive-summarizer
A POS-aware extractive text summarization system for Kannada using NLP techniques such as POS tagging, TF-IDF, and sentence ranking# POS-Aware Kannada Extractive Summarizer

## Overview

The rapid growth of online news has made it difficult for readers to quickly identify the most relevant information in lengthy articles. This project aims to develop a **POS-aware extractive text summarization system for Kannada**, capable of automatically identifying and extracting the most informative sentences from news articles.

Unlike abstractive summarization, extractive summarization selects important sentences directly from the original document while preserving grammatical correctness. Since Kannada is a low-resource language, there is limited availability of annotated datasets and summarization systems. This project addresses these challenges by creating a benchmark corpus, implementing robust preprocessing techniques, and evaluating multiple summarization algorithms.

---

## Problem Statement

With the abundance of Kannada news articles available online, manually reading entire articles to obtain the key information is time-consuming. The objective of this project is to automatically generate concise summaries by extracting the most significant sentences from Kannada news documents.

---

## Objectives

* Build a benchmark corpus of Kannada news articles,essay,stories.
* Develop preprocessing techniques for Kannada text.
* Implement a rule-based Kannada stemmer.
* Implement multiple extractive summarization algorithms.
* Compare supervised and unsupervised summarization approaches.
* Evaluate system performance using standard metrics.

---

## Dataset

The dataset consists of Kannada news articles collected from:

* Prajavani
* Kannada Prabha
* Kannada Wikipedia
* udayavani
* vijayavani
  

Approximately **400 news articles** are manually summarized by multiple annotators. Around **15% of the articles are shared among annotators** to measure inter-annotator agreement and establish a reliable gold-standard corpus.

---

## Methodology

### 1. Data Collection

* Collect Kannada news articles.
* Remove unwanted HTML and formatting.
* Normalize Unicode text.

### 2. Corpus Creation

* Sentence segmentation
* Tokenization
* Stop-word removal
* Manual annotation
* Inter-annotator agreement analysis

### 3. Rule-Based Kannada Stemmer

Develop a rule-based stemmer capable of handling Kannada suffixes and inflectional morphology.

### 4. Feature Extraction

The summarizer uses several statistical and linguistic features:

* TF (Term Frequency)
* IDF (Inverse Document Frequency)
* GSS Coefficient
* Sentence Position
* Sentence Length
* POS-based sentence importance

### 5. Summarization Algorithms

The project evaluates multiple extractive summarization techniques:

* TF-IDF Sentence Scoring
* GSS-based Keyword Extraction
* TextRank
* POS-aware Sentence Ranking

### 6. Evaluation

Generated summaries are compared against manually created summaries using:

* ROUGE-1
* ROUGE-2
* ROUGE-L
* Precision
* Recall
* F1 Score
* Inter-Annotator Agreement

---

## Project Structure

```
kannada-pos-extractive-summarizer/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── corpus/
│
├── src/
│   ├── preprocessing.py
│   ├── tokenizer.py
│   ├── stemmer.py
│   ├── pos_tagger.py
│   ├── tfidf.py
│   ├── textrank.py
│   ├── summarizer.py
│   └── evaluation.py
│
├── notebooks/
├── models/
├── results/
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Technologies

* Python
* Stanza
* Indic NLP Library
* Scikit-learn
* NetworkX
* Pandas
* NumPy

---

## Workflow

1. Collect Kannada news articles.
2. Preprocess the text.
3. Build an annotated corpus.
4. Apply POS tagging and stemming.
5. Extract keywords using TF-IDF and GSS.
6. Rank sentences using statistical and linguistic features.
7. Generate extractive summaries.
8. Evaluate against human-written summaries.

---

## Expected Outcomes

* A benchmark Kannada summarization corpus.
* A rule-based Kannada stemmer.
* Multiple extractive summarization models.
* Comparative evaluation of summarization techniques.
* A reproducible open-source implementation.

---

## Future Work

* Transformer-based abstractive summarization.
* BERT/mBERT-based sentence embeddings.
* Attention-based summarization models.
* Support for multilingual Indic languages.

---

## References

1. TF-IDF based Text Summarization
2. TextRank: Bringing Order into Text
3. Extractive Text Summarization Using Sentence Extraction
4. ROUGE Evaluation Metrics
5. GSS Coefficient-Based Keyword Extraction
6. Kannada NLP and Rule-Based Stemming Research
7. News articles (http://www.prajavani.net/ ,http://www.kannadaprabha.com/, https://epaper.vijayavani.net/,https://udayavani.com/) and wikipedia.


