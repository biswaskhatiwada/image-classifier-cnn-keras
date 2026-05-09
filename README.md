# Building an Image Classifier with CNNs and Keras

This is a class project for my AI course. It builds an image classifier to identify mushroom species using Convolutional Neural Networks (CNN) and Transfer Learning with Keras and TensorFlow.

## Project Overview

The project classifies mushroom images into 5 species:
- Agaricus
- Amanita
- Entoloma
- Hygrocybe
- Suillus

## What's Inside

### Model 1 — Custom CNN
A 3-block CNN built from scratch with:
- Conv2D + BatchNormalization layers
- MaxPooling and Dropout for regularization
- GlobalAveragePooling + Dense classifier head

### Model 2 — Transfer Learning (MobileNetV2)
A pretrained MobileNetV2 (ImageNet weights) with a custom classifier head. This model achieved ~80% validation accuracy, significantly outperforming the custom CNN.

## Dataset

The dataset contains 2,094 mushroom images split into:
- Train: 1,466 images
- Validation: 314 images
- Test: 314 images

Data augmentation (random flips, brightness, contrast, saturation) was applied to the training set.

## Results

| Model | Val Accuracy |
|-------|-------------|
| Custom CNN | ~32% |
| MobileNetV2 (Transfer Learning) | ~80% |

## Tech Stack

- Python 3.12
- TensorFlow 2.19 / Keras
- scikit-learn
- matplotlib / seaborn

## How to Run

1. Open `image_classifier_cnn_keras.ipynb` in Google Colab
2. Mount your Google Drive and place the dataset at `/content/drive/MyDrive/archive/Mushrooms`
3. Run all cells in order
