# 📘 Statistical Language Modeling using N-grams (Unigram, Bigram, Trigram)

## 📌 Overview

This project implements **statistical language models** using **unigrams, bigrams, and trigrams** on a literary English corpus sourced from **Project Gutenberg**.

The model estimates word sequence probabilities using **Laplace (Add-1) smoothing**, computes sentence probabilities, and performs **interactive next-word prediction** based on probabilistic context.

The goal of this project is to understand the **foundations of language modeling** used in early NLP systems and to gain hands-on experience with **probabilistic text modeling**.

---

## 📚 Corpus Details

The corpus is built by combining multiple **public-domain English novels** to ensure linguistic diversity and sufficient vocabulary coverage.

### Books Used
- *Pride and Prejudice* – Jane Austen  
- *Little Women* – Louisa May Alcott  
- *Alice’s Adventures in Wonderland* – Lewis Carroll  
- *The Adventures of Sherlock Holmes* – Arthur Conan Doyle  

All texts are sourced from **Project Gutenberg**.

---

## ⚙️ Preprocessing Steps

The following preprocessing steps are applied to the raw text:

- Conversion to lowercase  
- Removal of punctuation and non-alphabetic characters  
- Normalization of whitespace  
- Tokenization into word sequences  

---

## 🧠 Language Models Implemented

### 1️⃣ Unigram Model
- Counts individual word frequencies  
- Used for vocabulary statistics and fallback probabilities  

---

### 2️⃣ Bigram Model
- Models the conditional probability of a word given the previous word  
- Uses **Add-1 (Laplace) smoothing** to handle unseen word pairs  

**Formula:**

\[
P(w_2 \mid w_1) = \frac{C(w_1, w_2) + 1}{C(w_1) + V}
\]

---

### 3️⃣ Trigram Model
- Models the conditional probability of a word given the previous two words  
- Uses **Add-1 smoothing** and **backs off to the bigram model** for unseen contexts  

**Formula:**

\[
P(w_3 \mid w_1, w_2) = \frac{C(w_1, w_2, w_3) + 1}{C(w_1, w_2) + V}
\]

---

## ✨ Features

- ✔ Corpus construction from multiple books  
- ✔ Unigram, bigram, and trigram frequency computation  
- ✔ Add-1 smoothing for probability estimation  
- ✔ Sentence probability calculation using the bigram model  
- ✔ Interactive next-word prediction  
- ✔ Backoff strategy for unseen trigram contexts  

---

## 🖥️ Interactive Next-Word Prediction

The program allows users to input:

- **One word** → predicts the next word using the **bigram model**  
- **Two words** → predicts the next word using the **trigram model**


---

## 🛠️ Technologies Used

- Python  
- Regular Expressions (`re`)  
- `collections.Counter`  
- HTTP requests (`requests`)  
- Project Gutenberg corpus  

---

## 📈 Learning Outcomes

Through this project, I learned:

- How statistical language models work internally  
- The data sparsity problem in NLP  
- The role of smoothing in probability estimation  
- Differences between unigram, bigram, and trigram contexts  
- How early language models differ from modern neural models  

---

## 📌 Future Improvements

- Perplexity evaluation  
- Text generation using n-gram sampling  
- Comparison with neural language models (LSTM / Transformer)  
- `<UNK>` token handling for out-of-vocabulary words  
- GUI or web-based interface  

---

## 📜 License

All texts used are from **Project Gutenberg** and are in the public domain.  
This project is intended for **educational and academic purposes**.

