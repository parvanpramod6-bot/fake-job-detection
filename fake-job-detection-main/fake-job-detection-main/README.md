# 🔍 Fake Job Posting Detection

A machine learning project to detect fraudulent job postings using NLP techniques.

## 📊 Dataset
- Source: EMSCAD Dataset (Kaggle)
- Total Records: 17,880 job postings
- Legitimate: 17,014 (95.2%)
- Fraudulent: 866 (4.8%)

## 🔧 Techniques Used
- Text Preprocessing (cleaning, lowercasing, removing URLs)
- TF-IDF Vectorization (bigrams, 10,000 features)
- CountVectorizer (for comparison)

## 🤖 Models Implemented
| Model | F1-Score |
|-------|----------|
| Linear SVM (TF-IDF) | 0.855 |
| Logistic Regression (Count) | 0.846 |
| Naive Bayes (TF-IDF) | 0.754 |
| Logistic Regression (TF-IDF) | 0.638 |
| Naive Bayes (Count) | 0.521 |
| Complement NB (TF-IDF) | 0.495 |

## 🏆 Best Model
**Linear SVM (TF-IDF)**
- Accuracy : 98.8%
- Precision : 99.2%
- Recall : 75.1%
- F1-Score : 85.5%

## 💡 Key Findings
- Fraudulent jobs have much shorter company profiles (231 vs 641 chars)
- Fake postings use urgency language and unrealistic earning claims
- Preprocessing improved F1-Score by +0.169 (36% better fraud detection)
- Accuracy alone is misleading — F1-Score is the right metric here

## ⚠️ Limitations
- Dataset imbalance (4.8% fraud) affects recall
- Model may miss sophisticated fake postings
- Needs periodic retraining as fraud patterns evolve
- Does not verify company existence externally

## 🛠️ Tools & Libraries
Python, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, WordCloud

## 👨‍💻 Author
Pavanprasad1
