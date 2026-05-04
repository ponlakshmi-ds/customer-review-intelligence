# Customer Review Intelligence

## LLM-Assisted NLP for Business Insight Extraction

## Overview

This project explores how **customer review data can be transformed into structured operational insight** using a combination of classical NLP, transformer-based topic modelling, emotion analysis, and local LLM-assisted topic abstraction.

The goal was not simply to classify sentiment, but to design an **insight generation workflow** capable of identifying recurring service issues, uncovering customer pain points, and translating large volumes of unstructured feedback into actionable business recommendations.

The project compares multiple analytical approaches — from statistical topic modelling to embedding-based clustering and LLM-driven synthesis — to evaluate which methods produce the most interpretable and decision-useful insights.

---

## Business Problem

Organisations receive large volumes of customer feedback through review platforms such as Google Reviews and Trustpilot.

While this feedback contains valuable operational insight, it is difficult to analyse at scale because:

* reviews are unstructured text
* complaints often describe overlapping issues
* sentiment alone does not explain root causes
* recurring themes may vary across locations
* large datasets make manual review impractical

The objective of this project was to build a pipeline that could:

✅ identify recurring complaint themes

✅ segment insights by location / branch

✅ understand emotional drivers behind negative reviews

✅ compare topic modelling approaches

✅ generate business-facing recommendations

---

## Methodology

### 1. Text Preprocessing

Reviews were cleaned and normalised using:

* regex-based cleaning
* tokenisation
* stopword removal
* case normalisation
* NLP preprocessing using NLTK

Exploratory analysis included:

* frequency distributions
* word clouds
* phrase pattern exploration

---

### 2. Topic Modelling Comparison

Multiple approaches were evaluated.

#### BERTopic

Embedding-based clustering for semantically coherent topic discovery.

Used for:

* dynamic topic formation
* interpretable cluster discovery
* branch/location-level segmentation

Visual diagnostics included:

* Intertopic Distance Map
* Topic Bar Charts
* Topic Heatmaps

---

#### LDA Baseline

Used as a classical benchmark topic model for comparison.

This provided a baseline against embedding-driven approaches.

---

### 3. Emotion Analysis

Emotion classification was performed using:

**bhadresh-savani/bert-base-uncased-emotion**

This added richer behavioural context beyond positive/negative sentiment by identifying emotional patterns such as:

* anger
* frustration
* disappointment
* satisfaction
* excitement

Emotion-aware filtering helped isolate operationally meaningful complaint themes.

---

### 4. LLM-Assisted Topic Abstraction

A local LLM workflow was developed in Google Colab using:

**Qwen2.5-3B-Instruct**

This layer was used for:

* clearer topic naming
* summarisation of complaint clusters
* abstraction of recurring operational themes
* generation of recommendation-oriented outputs

Multiple local model options were explored before selecting Qwen for:

* better prompt adherence
* efficient inference
* practical Colab execution

---

## Key Findings

The strongest analytical workflow was:

> **BERTopic clustering + LLM-assisted topic abstraction**

This produced:

* clearer thematic separation
* better interpretability
* stronger business relevance
* more actionable recommendations than traditional topic modelling alone

A major learning was that:

> **classical NLP + modern embeddings + LLM synthesis produces richer operational insight than any single method individually**

---

## My Contribution

This was an end-to-end individual project where I independently led:

* data collection and cleaning
* exploratory text analysis
* NLP preprocessing
* BERTopic modelling
* emotion analysis pipeline design
* LLM experimentation and prompting
* model comparison and evaluation
* business recommendation synthesis
* insight visualisation and reporting

---

## Technologies Used

* Python
* Pandas
* NLTK
* Regular Expressions (re)
* BERTopic
* Transformer embeddings
* Emotion classification (BERT)
* Qwen2.5-3B-Instruct
* Matplotlib
* WordCloud

---

## Key Learnings

This project strengthened my understanding of:

* modern topic modelling workflows
* embedding-driven semantic clustering
* emotional context in text analytics
* prompt design for insight synthesis
* combining classical NLP with LLM workflows
* translating text analytics into business recommendations

The biggest takeaway was:

> **The value of NLP is not just extracting themes — it is structuring unstructured customer voice into decision-support insight.**
