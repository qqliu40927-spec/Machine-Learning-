# RC18 Machine Learning  
## Pix2Pix-Based Satellite Image Colorization

---

## 1. Project Overview

This project explores **image-to-image translation** using deep learning models including **Pix2Pix, CycleGAN, and Colorization networks**.

The main objective is to transform **grayscale satellite imagery into color images**, enabling enhanced visual interpretation of urban and environmental data.

---

## 2. Framework Logic

The project follows a modular pipeline:
## 3. Workflow

The project follows a standard Pix2Pix pipeline:

1. Data Preparation  
   Paired images are organised in AB format.

2. Training  
   The model is trained using a Pix2Pix architecture based on a U-Net generator and PatchGAN discriminator.

3. Testing  
   The trained model is used to generate outputs from unseen test images.

4. Output  
   Results are automatically saved as images and HTML pages.
   ## 4. How to Run

Install dependencies:

```bash
pip install -r requirements.txt
python train.py --dataroot ./datasets/AB --name first_run --model pix2pix

## 5. Results

Below are sample outputs from the Pix2Pix model:

| Input | Generated | Ground Truth |
|------|----------|--------------|
| ![](results/example_1_input.png) | ![](results/example_1_fake.png) | ![](results/example_1_real.png) |
| ![](results/example_2_input.png) | ![](results/example_2_fake.png) | ![](results/example_2_real.png) |

The results demonstrate how the model learns spatial and visual relationships from paired data.
