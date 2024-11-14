# Supervised, Semi-Supervised, and Unsupervised Learning on Breast Cancer Dataset

This project focuses on classifying breast cancer diagnoses using different learning approaches: supervised, semi-supervised, and unsupervised. Additionally, active and passive learning approaches are applied to a banknote authentication dataset. This project is part of Homework 8 for the DSCI 552 course.

## Table of Contents
- [Project Overview](#project-overview)
- [Datasets](#datasets)
- [Learning Approaches](#learning-approaches)
- [Active Learning](#active-learning)
- [Requirements](#requirements)

## Project Overview
The primary objectives of this project are:
1. To compare supervised, semi-supervised, and unsupervised learning methods on a breast cancer classification task.
2. To evaluate model performance using metrics such as accuracy, precision, recall, F1-score, AUC, and ROC.
3. To implement active and passive learning approaches using SVMs on the banknote authentication dataset.

## Datasets
1. **Breast Cancer Wisconsin (Diagnostic) Data Set**:
   - [Dataset Link](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
   - Includes 569 instances with 30 attributes and binary labels (Benign, Malignant).

2. **Banknote Authentication Data Set**:
   - [Dataset Link](https://archive.ics.uci.edu/ml/datasets/banknote+authentication)
   - Used to compare active and passive learning methods with SVMs.

## Learning Approaches
1. **Supervised Learning**:
   - L1-penalized SVM is trained with cross-validation to classify the data.
   - Performance metrics such as accuracy, precision, recall, F1-score, and AUC are calculated across multiple Monte-Carlo runs.
   
2. **Semi-Supervised Learning (Self-training)**:
   - A portion of the data is labeled, while the rest is treated as unlabeled.
   - Unlabeled data points are iteratively classified and added to the labeled set until all data points are used.

3. **Unsupervised Learning (Clustering)**:
   - K-means clustering is applied with k=2, and clusters are labeled based on a majority poll.
   - Spectral clustering is also applied using an RBF kernel to identify non-convex clusters.

## Active Learning
1. **Passive Learning**:
   - Incremental training with randomly selected data points added in stages.
   - Test error is calculated at each stage, producing a learning curve.
   
2. **Active Learning**:
   - Data points closest to the decision boundary are incrementally added to the training set.
   - Performance is tracked and compared with passive learning to evaluate effectiveness.

3. **Comparison**:
   - Monte Carlo simulations are used to average test errors over multiple runs.
   - Learning curves are plotted to illustrate the differences between active and passive learning.

## Requirements
The project requires:
- Python
- Libraries: `numpy`, `pandas`, `matplotlib`, `sklearn`