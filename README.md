# MovieLens Recommender System

A comprehensive end-to-end **Recommender System** built using the MovieLens dataset.
This project implements multiple recommendation techniques including:

* Content-Based Filtering
* Collaborative Filtering (User & Item based)
* Matrix Factorization (SVD)
* Hybrid Recommendation System
* Neural Network Recommender
* Reinforcement Learning (Bandit & Q-Learning)
* Explainable AI (SHAP, Feature & Neighborhood explanations)

---

## Project Overview

Recommender systems are widely used in platforms like Netflix, Amazon, and Spotify.
This project explores different recommendation approaches and compares their performance and behavior.

The system progressively evolves from simple similarity-based models to advanced deep learning and reinforcement learning methods.

---

##  Project Structure

```
MovieLens-Recommender-System/
│
├── dataset/
│   ├── movies.csv
│   ├── ratings.csv
│   ├── tags.csv
│   └── links.csv
│
├── recommender_system.ipynb
├── README.md
└── requirements.txt
```

---

##  Setup Instructions


###  Create Environment (Optional but Recommended)

Using **conda**:

```
conda create -n recommender python=3.10
conda activate recommender
```

---

### Install Dependencies

```
pip install -r requirements.txt
```



##  Features Implemented

###  1. Content-Based Filtering

* TF-IDF vectorization of movie genres
* Cosine similarity for recommendations

---

###  2. User Profile Recommender

* Builds personalized user profiles
* Weighted by user ratings

---

### 3. Collaborative Filtering

####  User-Based CF

* Finds similar users
* Predicts ratings based on neighbors

####  Item-Based CF

* Finds similar movies
* Recommends based on item similarity

---

###  4. Matrix Factorization

####  SVD (Manual)

* Decomposes user-item matrix
* Learns latent features

####  Surprise Library SVD

* Efficient implementation
* RMSE evaluation (~0.87)

---

###  5. Hybrid Recommendation System


 Optimization:

* Applied hybrid scoring only on top candidate movies for efficiency

---

###  6. Neural Network Recommender

* Built using TensorFlow/Keras
* Learns:

  * User embeddings
  * Movie embeddings

Architecture:

```
User Features → Dense → Embedding
Movie Features → Dense → Embedding
        ↓
    Concatenate
        ↓
   Dense Layers
        ↓
   Predicted Rating
```

---

### 7. Reinforcement Learning Recommender

####  Multi-Armed Bandit

* ε-greedy strategy
* Balances exploration vs exploitation

####  Q-Learning

* Learns optimal recommendation policy
* Updates Q-values based on rewards

---

###  8. Explainable AI

####  Feature-Based Explanation

* Explains recommendations using genres

####  Neighborhood Explanation

* Shows similar movies

####  SHAP (Model-Agnostic)

* Explains neural network predictions
* Identifies important features

 Insight:
Genres like **Action, Sci-Fi, Comedy, and Romance** strongly influence predictions.

---

## Sample Results

* Content-based recommendations show high similarity for similar genres
* Collaborative filtering captures user behavior patterns
* Hybrid model improves recommendation quality
* Neural model achieves strong learning of user preferences
* RL models adapt recommendations based on feedback

---

##  Key Learnings

* Different recommendation techniques have unique strengths
* Hybrid models provide better performance
* Deep learning captures complex patterns
* Explainability improves trust in recommendations
* Optimization is crucial for scalability

---

