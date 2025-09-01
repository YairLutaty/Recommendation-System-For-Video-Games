# Recommendation System for Video Games  

This project was developed as part of my **Data Science Workshop** at the Open University of Israel.  
It explores how **machine learning and recommender systems** can be applied in the video game industry to improve player experience and support business goals.  

The focus is on designing a system that can recommend **the 10 most relevant games for each user** — not just predicting ratings, but identifying games that a user is **most likely to purchase**.  

---

## Project Goals  

- Build a **recommendation system** tailored for video games, a domain with unique challenges compared to movies or music (e.g., games are longer, expensive, and more diverse in style).  
- Explore different recommendation approaches:  
  - **Collaborative Filtering** (learning from user–item interactions)  
  - **Content-Based Filtering** (using game metadata & embeddings)  
  - **Hybrid methods** (combining both)  
- Incorporate **Natural Language Processing (NLP)** by analyzing review texts and sentiments to better capture player opinions.  
- Evaluate recommendations not only by accuracy, but also by **hit rate** and **purchase likelihood**.  

---

## 📊 Dataset  

We use the [Amazon Reviews 2023 – Video Games subset](https://amazon-reviews-2023.github.io/):  

- **~50K reviews** of video games, all marked as confirmed purchases.  
- Each review contains:  
  - ⭐ Rating  
  - 📝 Review text + embeddings  
  - ✅ Sentiment (predicted via Hugging Face models)  
- Metadata includes:  
  - 🎮 Game title and description  
  - 📦 Features (platform, genre, publisher, etc.)  
  - 🔗 Description embeddings (1024-d vectors for similarity search)  

Users on average review ~5 games, giving us enough history for training and evaluation.  

---

## What We Explore  

1. **Recommendation Accuracy**  
   - Does collaborative filtering outperform content-based methods?  
   - How effective are hybrid approaches?  

2. **Purchase Prediction**  
   - Can we ensure at least one recommendation per user matches a real purchase from the test set?  
   - How well do models capture user intent beyond ratings?  

3. **User Behavior Insights**  
   - What trends exist in player preferences across genres/platforms?  
   - How do sentiment scores align with numerical ratings?  

4. **Business Perspective**  
   - How can recommendations increase the likelihood of purchase?  
   - Which recommendation strategies are most suitable for video game platforms (e.g., Steam, Xbox Store)?  

---

## 📖 About the Notebook  

The main work is in **`Data_Science_Workshop.ipynb`**, but GitHub’s viewer cannot fully render it due to the use of **ipywidgets** (interactive visualizations).  
To make the project accessible, three versions are provided:  

### 1. Code-Only (GitHub-Friendly) Notebook  
- **`Data_Science_Workshop_no_outputs.ipynb`**  
- Contains all code and explanations.  
- Opens on GitHub without issues.  
- No executed outputs or widget interactivity.  

### 2. Full Notebook (with Outputs & Widgets)  
- **`Data_Science_Workshop.ipynb`**  
- Contains the **complete workflow**: preprocessing, visualizations, recommendation models, widgets.  
- May not render properly on GitHub.  

### 3. Full Notebook (Online via nbviewer)  
[View the full notebook on nbviewer](https://nbviewer.org/github/YairLutaty/Recommendation-System-For-Video-Games/blob/main/Data_Science_Workshop.ipynb)  
- Supports rendered outputs and widget states.  

---

## 🚀 Run It Yourself  

For the best experience, run the notebook interactively:  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/YairLutaty/Recommendation-System-For-Video-Games/HEAD?labpath=Data_Science_Workshop.ipynb)  

*(Launching may take a few minutes)*  

---

## 🛠️ Tech Stack  

- **Languages & Tools**: Python, Jupyter, GitHub, Binder  
- **Data Processing**: Pandas, NumPy  
- **Machine Learning**: Scikit-learn, PyTorch, LightGBM  
- **Recommender Systems**: ALS, BPR, Neural Collaborative Filtering  
- **NLP & Embeddings**: Hugging Face models, Sentence Transformers  
- **Visualization**: Matplotlib, Seaborn, ipywidgets  
