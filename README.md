# Recommendation Systems Project

This repository contains a comprehensive exploration of different types of recommendation systems, including **Collaborative Filtering**, **Content-Based Filtering**, and a **Hybrid Approach**. The project demonstrates key concepts in building, evaluating, and deploying recommendation algorithms, with a focus on real-world application scenarios.

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Datasets](#datasets)
4. [Methods](#methods)
    - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis)
    - [Collaborative Filtering](#collaborative-filtering)
    - [Content-Based Filtering](#content-based-filtering)
    - [Hybrid Recommendation System](#hybrid-recommendation-system)
5. [Setup and Installation](#setup-and-installation)
6. [Usage](#usage)
7. [Results and Insights](#results-and-insights)

---

## Introduction

This project aims to build robust recommendation systems to provide personalized suggestions for users. It covers:
- **Collaborative Filtering**: Based on user-item interactions.
- **Content-Based Filtering**: Leverages item features like genres and tags.
- **Hybrid Model**: Combines both approaches for improved performance.

## Project Structure

The repository is organized as follows:
```plaintext
.
├── notebooks/
│   ├── eda.ipynb                        # Exploratory Data Analysis
│   ├── data_preprocessing.ipynb         # Data preprocessing and feature engineering
│   ├── collaborative_filtering_modeling.ipynb # Collaborative Filtering with SVD
│   ├── content_based_filtering_modeling.ipynb # Content-Based Filtering with TF-IDF and cosine similarity
│   ├── hybrid_modeling.ipynb            # Hybrid recommendation system
├── data/
│   ├── ratings.csv                      # User ratings dataset
│   ├── movies.csv                       # Movies dataset with genres
│   ├── tags.csv                         # Tags dataset
└── README.md                            # Project documentation (this file)
```
## Datasets

- **Ratings**: Contains user ratings for movies.
- **Movies**: Includes movie metadata like titles and genres.
- **Tags**: User-provided tags for movies.

Data preprocessing steps include:
- Handling missing values in genres and tags.
- One-hot encoding genres.
- Vectorizing tags using TF-IDF.

## Methods

### Exploratory Data Analysis (EDA)
Initial analysis and visualization of datasets to understand user behavior, movie popularity, and rating distributions.

### Collaborative Filtering
Implemented using **Singular Value Decomposition (SVD)**:
- Optimized with **GridSearchCV** to find the best parameters for:
  - Number of latent factors.
  - Learning rate.
  - Regularization.
  - Number of epochs.

### Content-Based Filtering
- Genres were **one-hot encoded** using `MultiLabelBinarizer`.
- Tags were vectorized using **TF-IDF**.
- **Cosine similarity** calculated between movies based on combined features.

### Hybrid Recommendation System
- Combines collaborative and content-based filtering to improve recommendations.
- Maps `movieId` to indices for matrix-based operations.

## Results and Insights

- **Collaborative Filtering**: Achieved optimal performance with tuned hyperparameters.
- **Content-Based Filtering**: Recommendations aligned well with user interests by leveraging genre and tag data.
- **Hybrid Model**: Successfully combined user preferences and content similarity for enhanced results.

## Future Work

- **Tuning and evaluation of the content-based/hybrid recommendation models.**
- Incorporate deep learning-based recommendation models.
- Evaluate scalability with larger datasets.
- Deploy models using a REST API for real-time recommendations.
