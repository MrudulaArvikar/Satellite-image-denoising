# Satellite Image Denoising Project

This project implements a Denoising Autoencoder to remove noise from satellite images. The model processes noisy images, removes the noise, and outputs denoised images with improved quality, evaluated using the PSNR (Peak Signal-to-Noise Ratio) metric. The entire project code has been adapted from a publicly available repository.

## Features

- **Denoising Autoencoder Model**: A convolutional neural network (CNN) designed for noise reduction.
- **Patch-Based Processing**: Handles large satellite images by splitting them into smaller patches for efficient processing.
- **Training and Evaluation**: Train the model on noisy and clean image pairs and evaluate the quality using PSNR.
- **Utilities for Image Patching**: Includes scripts to split large images into manageable patches for processing.

## Project Source

This project is based entirely on the work available at [Satellite Image Denoising GitHub Repository](#). Full credit goes to the repository's author for the code and methodology.

## Usage

### Prerequisites

- Python 3.x
- PyTorch
- torchvision
- Pillow
- numpy
- matplotlib

Install the dependencies:

##Dataset
Noisy and clean satellite images are required in separate directories:

/path/to/noisy - Noisy images
/path/to/clean - Clean images

##Steps to Run
1. Training the Model
Update the paths to the noisy and clean image folders in the script.
Train the denoising autoencoder by running:

python train_autoencoder.py
The trained model will be saved as denoising_model.pth.

2. Inference
Provide the path to the noisy image for testing.
Run the inference script to denoise the image:
bash

python infer_autoencoder.py
The denoised image will be saved, and PSNR values will be displayed.

3. Handling Large Images
Use the patching script to divide large images into smaller patches:
bash

python patching.py
Denoise each patch and combine them to reconstruct the full image.
Credits

The code and methodology for this project are credited entirely to Shantanu Shrivastava's Satellite Image Denoising Repository.


