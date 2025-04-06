# MNIST Digit Classifier

A simple neural network built from scratch in Python to classify handwritten digits (0-9) from the MNIST dataset.

## Overview

This project trains a basic two-layer neural network to recognize digits using gradient descent. It processes the MNIST dataset, trains the model, and prints accuracy during training.

## Features

- Loads MNIST data from a CSV file.
- Splits data into training (59,000 samples) and test (1,000 samples) sets.
- Normalizes pixel values for better training.
- Uses a 2-layer neural network with ReLU and softmax activations.
- Trains with gradient descent and shows accuracy progress.

## Requirements

- Python 3.x
- Libraries: `numpy`, `pandas`, `sklearn`


## How It Works

### Data Preparation
- Reads `mnist_train.csv`.
- Shuffles data and splits into train (59,000) and test (1,000) sets.
- Normalizes pixel values (divides by 255).

### Model
- **Layer 1**: 784 inputs (pixels) → 10 neurons (ReLU activation).
- **Layer 2**: 10 neurons → 10 outputs (softmax activation for probabilities).

### Training
- Uses gradient descent with 500 iterations and a 0.1 learning rate.
- Updates weights and biases using forward and backward propagation.
- Prints accuracy every 10 iterations.

### Functions
- `initialize_parameters()`: Sets random weights and zero biases.
- `encode_labels()`: Converts labels to one-hot format.
- `forward_propagation()`: Computes activations through layers.
- `backward_propagation()`: Calculates gradients for updates.
- `update_parameters()`: Adjusts weights and biases.
- `get_predictions()`: Picks the most likely digit.
- `calculate_accuracy()`: Measures prediction accuracy.
- `gradient_descent()`: Runs the training loop.

## Results
After 500 iterations, the model typically achieves ~85-90% accuracy on the training set, and around ~88% on the test set.
