# ml-vs-dl-data-analysis
Comparative analysis of Machine Learning and Deep Learning models across tabular, image, and text data to evaluate model performance and data-driven model selection.

# Machine Learning vs Deep Learning Across Data Types

This project explores the performance comparison between traditional Machine Learning and Deep Learning models across three different types of data: tabular, image, and text.

The goal is to understand when deep learning provides significant improvements and when simpler models remain more effective.

---

## Project Overview

This project consists of three case studies:

1. **Tabular Data — Titanic Dataset**
2. **Image Data — MNIST Digit Recognition**
3. **Text Data — Disaster Tweets Classification**

Each case includes:
- Data preprocessing & feature engineering
- Model development (ML vs DL)
- Performance evaluation
- Error analysis

---

## Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib, Seaborn

---

## Case Study 1: Titanic (Tabular Data)

**Objective:** Predict passenger survival using structured data

### Key Steps:
- Handling missing values (Age, Embarked)
- Feature engineering (FamilySize, Title extraction)
- One-hot encoding & scaling

### Models:
- Logistic Regression → Accuracy: 0.8101
- Random Forest → **Accuracy: 0.8324 (Best)**
- MLP (Deep Learning) → Accuracy: 0.8212

### Insight:
- Random Forest outperformed deep learning
- Deep learning was less effective due to small dataset size (~891 rows)
- Feature engineering played a critical role

---

## Case Study 2: MNIST (Image Data)

**Objective:** Classify handwritten digits (0–9)

### Key Steps:
- Image normalization
- PCA for ML models
- Reshaping for CNN

### Models:
- PCA + SVM → Accuracy: 0.9777
- PCA + Random Forest → Accuracy: 0.9475
- CNN (Deep Learning) → **Accuracy: 0.9840 (Best)**

### Insight:
- CNN achieved the highest accuracy
- Deep learning excels in capturing spatial patterns
- Trade-off: higher accuracy but longer training time

---

## Case Study 3: Disaster Tweets (Text Data)

**Objective:** Classify tweets as disaster-related or not

### Key Steps:
- Text cleaning (remove URL, mentions, noise)
- TF-IDF vectorization

### Models:
- Logistic Regression → **F1 Score: 0.75 (Best)**
- Naive Bayes → F1 Score: 0.735
- LSTM (Deep Learning) → F1 Score: 0.705

### Insight:
- Traditional ML outperformed deep learning
- Dataset size (~7.6k) was insufficient for LSTM
- TF-IDF proved effective for short text classification

---

## Key Takeaways

- There is no one-size-fits-all model
- Model performance depends heavily on:
  - Data type
  - Dataset size
  - Feature complexity

### Summary:
- Tabular → ML > DL  
- Image → DL > ML  
- Text (small dataset) → ML > DL  

---

## Business Insight

This project highlights the importance of selecting the right model based on data characteristics rather than assuming deep learning is always superior.
