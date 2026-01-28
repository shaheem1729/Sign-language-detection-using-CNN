# 🤟 Sign Language Recognition using CNN

A deep learning project that recognizes American Sign Language (ASL) gestures from images using a Convolutional Neural Network (CNN). This model aims to support real-time communication between the hearing and speech-impaired and others by translating signs into recognizable characters or words.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Evaluation](#evaluation)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [License](#license)

---

## 🧠 Overview

This project implements a CNN-based image classifier to detect and classify hand gestures representing ASL alphabets. It processes grayscale or RGB images of hand signs and outputs the corresponding letter.

---

## ✅ Features

- Classification of ASL letters using CNN
- Image preprocessing (resizing, normalization)
- Training & validation with performance metrics
- Confusion matrix and accuracy/precision/recall reports
- Simple user interface for predictions 

---

## 📊 Dataset

- **Source**: [ASL Alphabet Dataset](https://www.kaggle.com/grassknoted/asl-alphabet)
- **Content**: 
  - Images of hands showing ASL letters A-Z
  - ~87,000 training images (200x200 px)
  - 29 classes (A–Z, excluding J and Z due to motion)
- **Preprocessing**:
  - Resize to 64x64 or 128x128
  - Normalization (pixel values scaled between 0–1)
  - One-hot encoding for labels

---

## 🧱 Model Architecture

```text
Input -> Conv2D -> ReLU -> MaxPool -> Conv2D -> ReLU -> MaxPool -> Flatten -> Dense -> Dropout -> Dense (Softmax)
