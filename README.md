
# 🎮 Game Difficulty Adjuster (Machine Learning-Based DDA System)

## 📖 Overview
This project presents a machine learning-based Dynamic Difficulty Adjustment (DDA) system designed for puzzle games. The goal is to personalize the gameplay experience by adapting difficulty levels in real-time based on player performance and behavioral patterns.

A synthetic dataset of 30,000 gameplay records was generated to simulate realistic player behavior. The system combines unsupervised learning (K-Means clustering) and supervised learning (Random Forest classification) to model player skills and predict the optimal difficulty level.

---

## 🎯 Objectives
- Design an adaptive difficulty system for puzzle games  
- Model player behavior using gameplay metrics  
- Classify players into skill levels  
- Predict optimal difficulty (Easy, Medium, Hard)  
- Improve player engagement and reduce frustration  

---

## 🧠 Methodology

### 1. Synthetic Data Generation
- Created a dataset of 30,000 simulated gameplay records  
- Features include: accuracy, solving time, attempts, hints, score, and behavior trends  

### 2. Feature Engineering & Player Profiling
- Aggregated player-level statistics (average accuracy, time, etc.)  
- Computed learning progression using linear regression (learning slope)  

### 3. Player Clustering (K-Means)
- Applied K-Means clustering to group players into 5 skill levels  
- Ranked clusters from lowest to highest skill  

### 4. Target Creation
- Generated "optimal difficulty" labels using a scoring function  
- Reduced 5 clusters into 3 difficulty levels: Easy, Medium, Hard  

### 5. Classification Model (Random Forest)
- Trained a Random Forest classifier (200 trees)  
- Used gameplay + behavioral + cluster features  
- Dataset split: 90% training / 10% testing (by player ID)  

### 6. Simulation (Before vs After DDA)
- Compared player performance before and after applying DDA  
- Metrics: success rate, attempts, solving time  

---

## 📊 Results
- Accuracy: 98.5%  
- Balanced performance across all classes (F1-score ≈ 0.96+)  
- Improved success rate after DDA  
- Reduced number of attempts  
- More balanced and fair gameplay experience  

---

## ⚙️ Technologies Used
- Python  
- Scikit-learn  
- Pandas  
- NumPy  
- Matplotlib  

---

## 🚀 Key Features
- Combines clustering + classification  
- Handles both short-term and long-term player behavior  
- Interpretable model (Random Forest feature importance)  
- Scalable and adaptable to different puzzle games  
- Includes simulation to evaluate real impact  

---

## 🔍 Problem Solved
Traditional games use static difficulty, which leads to:
- Player frustration (too hard)  
- Player boredom (too easy)  

This project solves this by dynamically adjusting difficulty based on player performance.

---

## 📈 Future Work
- Use real player data instead of synthetic data  
- Implement real-time difficulty adjustment  
- Explore reinforcement learning approaches  
- Incorporate emotional/engagement signals  

---

## 📌 Conclusion
The proposed system successfully demonstrates how machine learning can be used to create a personalized and balanced gaming experience. By combining clustering and classification, the model adapts difficulty effectively and improves overall player engagement.
