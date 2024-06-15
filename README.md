# Advanced Topics in_ML

This project implements PonderNet, an innovative algorithm based on the research of Andrea Banino, Jan Balaguer, and Charles Blundell from DeepMind. PonderNet dynamically adjusts the number of computational steps based on the complexity of the given problem, balancing prediction accuracy, computational cost, and generalization.

:warning: This repository was created for the ATML (Advanced Topic in Machine Learning) course project.

:no_entry_sign: It is not intended for reuse.

:heart: Special thanks to my team mates [Jacopo Di Ventura ](https://github.com/JacopoD) and [Matteo Martinoli](https://github.com/MartinoliMatteo) for their contributions.

## Abstract
PonderNet dynamically adjusts computational steps to optimize performance in real-time. This project replicates and expands on the findings of the original research, applying PonderNet to the MNIST dataset and a parity task to evaluate its performance.

## Methodology
### Problem Setting
The goal is to learn a function that maps input values to corresponding output values using a neural network architecture with a custom loss function.

### Step Recurrence and Halting Process
The architecture consists of a step function and an initial state, generating predictions and halting probabilities. A Markov process with a Bernoulli random variable determines whether to continue or halt at each step.

### Training Loss
The total loss function combines reconstruction loss and a regularization term, with the regularization term encouraging exploration and balancing computational steps.

### Evaluation Sampling
During inference, the network dynamically decides whether to continue or halt at each step, optimizing computational efficiency.

## Implementation
### MNIST
The initial implementation uses the MNIST dataset to understand and validate the architecture. The model uses a Convolutional Neural Network (CNN) for feature extraction and a Multi-Layer Perceptron (MLP) for dynamic decision-making.

### Parity Task
The parity task involves binary classification, determining the parity of a vector of binary digits. The implementation uses a Gated Recurrent Unit (GRU) cell for its efficiency in capturing sequential dependencies.

## Results
### Beta's Influence on Halting Step Distribution
Analysis of the model's response to the geometric distribution shows varying impacts on the halting step distribution across different tasks.

### Number of Computational Steps
The model reduces computational steps without compromising accuracy, demonstrating PonderNet's efficiency.

## Discussion and Conclusion
PonderNet effectively balances computational steps and model accuracy. The project's implementation confirms the original paper's claims, highlighting the importance of hyper-parameter tuning for optimal performance.
