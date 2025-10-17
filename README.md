# Handwritten Digit Classification using keras

This project focuses on building an image classification system capable of recognizing handwritten digits (0–9) using neural networks. The goal is to compare and refine different models to achieve high accuracy on the MNIST dataset.

## Problem Statement

The task is to accurately classify grayscale images of handwritten digits. The MNIST dataset is used as a benchmark for training and evaluation.

* **Training Data:** 60,000 images (28x28 pixels)
* **Testing Data:** 10,000 images (28x28 pixels)

All image pixel values were normalized to the range **0–1** before training to improve model performance.

## Models & Methodology

Two neural network architectures were implemented and compared:

1. **Simple Neural Network (ANN)**

   * A fully-connected network with one hidden layer.
   * Serves as a baseline model.

2. **Convolutional Neural Network (CNN)**

   * Designed specifically for image data.
   * Includes convolutional layers for feature extraction and max-pooling layers to reduce dimensionality.

### Performance Enhancements

To further improve CNN performance, the following techniques were applied:

* **Data Augmentation:** Random rotations, shifts, and zooms were applied to artificially expand the training dataset, helping the model generalize better.
* **Hyperparameter Tuning:** Using Keras Tuner, the optimal combination of parameters (e.g., number of filters, learning rate) was automatically determined.

## Results

The models were evaluated based on test dataset accuracy:

| Model        | Test Accuracy |
| ------------ | ------------- |
| Simple ANN   | ~97.6%        |
| Baseline CNN | ~98.6%        |
| Tuned CNN    | ~99.2%        |

## Conclusion

The results demonstrate the advantage of using convolutional architectures and optimization techniques. The tuned CNN achieves the highest accuracy, making it highly effective for handwritten digit recognition.


