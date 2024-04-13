# LORA: Low-Rank Adaptation of Large Language Models implemented using PyTorch

## Overview

LORA is a technique for adapting large language models using low-rank approximation, implemented using PyTorch. This repository contains the code for applying LORA to the MNIST dataset, as well as explanations and examples to help you understand and use the technique effectively.

## Background

LORA (Low-Rank Adaptation) is a method for reducing the computational complexity of large language models by decomposing weight matrices into low-rank approximations. This allows for more efficient training and inference, especially in scenarios where computational resources are limited.
MNIST Dataset

The MNIST dataset consists of 28x28 pixel grayscale images of handwritten digits (0-9). It is commonly used as a benchmark dataset for image classification tasks and provides a suitable environment for testing the effectiveness of LORA.

## Implementation

The implementation of LORA in this repository is based on PyTorch, a popular deep learning framework. Here's a detailed overview of the key components:
1) Matrix Decomposition:
 - The weight matrices of the neural network model are decomposed into low-rank matrices using techniques like Singular Value Decomposition (SVD) or Alternating Least Squares    (ALS).
 - The decomposition process helps in reducing the computational complexity of the model while preserving important features.
2) Incremental Update:
- LORA allows for incremental updates to the low-rank matrices as new data is encountered during training.
- This is achieved by adding or modifying certain components of the decomposition to adapt to the new information without recalculating everything from scratch.
- Incremental updates help the model stay up-to-date with changing data distributions and improve its performance over time.

3) PyTorch Integration:
- The implementation leverages PyTorch's computational graph and autograd capabilities to efficiently compute gradients and perform backpropagation during training
- Custom layers and modules are implemented using PyTorch's nn.Module interface, making it easy to integrate LORA into existing neural network architectures.

4) Training Loop:
- The training loop orchestrates the process of loading data, forward and backward passes through the network, parameter updates, and evaluation.
- Techniques such as mini-batch processing, learning rate scheduling, and early stopping may be employed to improve training efficiency and performance.

## Files:
- lora.ipynb = contains the main file with the implementation of LoRa.
- svd.ipynb(Singular value decomposition) = contains the math behind the LoRa implementation. 

## Experiment and Customize:
Feel free to experiment with different hyperparameters, architectures, and datasets to see how LORA performs in various scenarios.Additionally, you can customize the implementation to suit your specific requirements by modifying the code or extending it with additional features.

## Acknowledgments

I would like to thank the open-source community for their contributions to PyTorch and other libraries that made this project possible. Additionally, I acknowledge the researchers and developers who have contributed to the advancement of techniques like low-rank approximation and its applications in machine learning.
Thanks to Umar Jamil for the tutorial on implementation of LoRA. <https://github.com/hkproj>

## Images
Fine Tuning 
![1](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/f083503e-d341-46f0-8cea-bf3fd6555eeb)
---

Problems with Fine Tuning 
![2](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/57e0513b-f55c-46da-9f54-8b0bdb251cec)
---

LoRA 
![3](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/259037f0-3c1d-4863-b179-f76b2723f5d6)
---

LoRa paper implementation
![4](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/f50c1467-c620-4126-92f4-79366d248627)
---

Total number of parameters
![5](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/7ed8f98b-5f43-4cee-8ba4-e1e0d01c5b1c)
---
Parameters introduced by LoRa addition 
![6](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/cb3e31fd-b171-4b11-be9b-74af1e5a91cc)
---
Error rate for the identification of each digit without the addition of LORA
![7](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/014f4e12-b4a6-401d-8fa1-f544bd1c9fb1)
---
Error rate for the identification of each digit with the addition of LORA
![8](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/0a54fccc-1741-4317-95c8-b06b91bc8a2f)
---
Total number of parameters to be saved drastically reduced
![9](https://github.com/dreamboat26/fuzzy-logic/assets/125608791/da0e78cb-d56e-489a-8079-14f92f60af8e)
---


