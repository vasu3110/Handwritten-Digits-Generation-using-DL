# Generative Adversarial Network (GAN) for Handwritten Digit Generation

## 🚀 Project Overview

This project implements a **Generative Adversarial Network (GAN)** to generate realistic handwritten digits based on the **MNIST dataset**.  
The GAN consists of two neural networks – a **generator** that creates synthetic digit images and a **discriminator** that distinguishes between real and generated digits.

## 🏗️ Model Architecture

The GAN model follows a two-network adversarial training setup:

- **Generator:** Takes random noise as input and generates digit-like images.
- **Discriminator:** Classifies images as real (from MNIST) or fake (from the generator).

### **Generator Architecture**

- Input: Random noise vector (latent space, e.g., 100-dimensional)
- Fully connected layers with **batch normalization** and **LeakyReLU activation**
- Deconvolution layers for upsampling
- Output: **28x28 grayscale image** of a handwritten digit

### **Discriminator Architecture**

- Input: **28x28 grayscale image**
- Convolutional layers with **LeakyReLU activation**
- Fully connected layers leading to a **sigmoid output (real/fake classification)**

## 📌 Features

✅ Implements a **Deep Convolutional GAN (DCGAN)** for enhanced image generation  
✅ Utilizes **Batch Normalization and Dropout** for training stability  
✅ Trains on the **MNIST dataset** containing **60,000 handwritten digit images**  
✅ Supports **custom dataset training and pretrained model checkpoints**  
✅ Provides **visualizations of training progress and generated digits**

## 📂 Dataset

The model is trained on **MNIST (Modified National Institute of Standards and Technology) dataset**, which consists of **28x28 grayscale images of handwritten digits (0-9)**.

- The dataset is preprocessed by **normalizing pixel values (0-1) and reshaping** the images.
- Training samples are loaded using the **TensorFlow/Keras `tf.keras.datasets.mnist` API**

## 🔧 Installation

To run this project, clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/GAN-MNIST.git
cd GAN-MNIST
pip install -r requirements.txt
```

📜 License
This project is licensed under the MIT License – see the LICENSE file for details.
