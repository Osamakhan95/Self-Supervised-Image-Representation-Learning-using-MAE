# Self-Supervised-Image-Representation-Learning-using-MAE
Generative AI Assignment
Self-Supervised Image Representation Learning using MAE

This project implements a Self-Supervised Masked Autoencoder (MAE) framework for learning visual representations from images without requiring labeled data. The system follows the MAE architecture where a large portion of image patches are masked and the model learns to reconstruct the missing patches.

Self-supervised learning allows deep learning models to extract meaningful features from large unlabeled datasets, which can later be used for downstream tasks such as classification, object detection, or segmentation. Masked Autoencoders are inspired by masked language modeling approaches used in NLP and apply a similar concept to images by masking image patches and predicting them.

In this project, approximately 75% of the image patches are masked, and the model is trained to reconstruct the original image from the remaining visible patches using an asymmetric encoder–decoder architecture.

Project Objective

The objective of this project is to design and implement a Masked Autoencoder based self-supervised learning system that can:

Learn useful visual representations without labeled data

Reconstruct masked image patches effectively

Capture semantic information from images

Demonstrate the effectiveness of self-supervised learning in computer vision tasks

The model learns representations that can later be used for downstream tasks such as image classification and feature extraction.

Architecture Overview

The implemented MAE system follows the standard masked autoencoder pipeline:

Image Patching
Input images are divided into fixed-size patches.

Random Masking
Around 75% of patches are randomly masked to create a challenging reconstruction task.

Encoder
The encoder processes only the visible patches, which reduces computational cost and forces the model to learn strong representations.

Decoder
A lightweight decoder receives encoded tokens along with mask tokens and reconstructs the original image.

Reconstruction Loss
The model is trained using a reconstruction loss (typically Mean Squared Error) between the original and reconstructed patches.

Key Features

Self-supervised learning approach (no labeled dataset required)

Masked Autoencoder architecture

Patch-based image representation

High masking ratio (75%)

Encoder–decoder transformer-based framework

Reconstruction-based training objective

Project Structure
Self-Supervised-Image-Representation-Learning-using-MAE
│
├── dataset/
│   ├── train/
│   └── test/
│
├── models/
│   └── mae_model.py
│
├── utils/
│   ├── data_loader.py
│   └── helper_functions.py
│
├── train.py
├── test.py
├── requirements.txt
└── README.md
Installation

Clone the repository:

git clone https://github.com/Osamakhan95/Self-Supervised-Image-Representation-Learning-using-MAE.git
cd Self-Supervised-Image-Representation-Learning-using-MAE

Install dependencies:

pip install -r requirements.txt
Dataset

The model can be trained on any image dataset.

Steps to prepare dataset:

Place training images inside the dataset folder.

Ensure images are properly formatted.

Training

To train the MAE model:

python train.py

The training process performs:

Patch extraction

Random masking

Encoder feature learning

Decoder reconstruction

Loss optimization

Testing / Reconstruction

To evaluate reconstruction results:

python test.py

The output will show reconstructed images compared with original inputs.

Results

The model successfully learns visual representations by reconstructing masked image patches.

Key observations:

High masking ratio encourages learning meaningful features.

The encoder learns generalizable representations.

Reconstruction quality improves as training progresses.

Applications

The learned representations can be used for:

Image classification

Transfer learning

Object detection

Medical image analysis

Feature extraction for computer vision tasks

Technologies Used

Python

PyTorch

NumPy

OpenCV / PIL

Matplotlib

Future Improvements

Possible extensions for this project include:

Using Vision Transformers (ViT) for the encoder

Fine-tuning the model for classification tasks

Training on larger datasets such as ImageNet

Implementing advanced MAE variants

Author

Osama Khan

GitHub:
https://github.com/Osamakhan95

If you want, I can also create a much better GitHub README with:

badges (Python, PyTorch, License)

architecture diagram

reconstruction image examples

training result graphs

That version looks much more professional for portfolio or AI research projects.
