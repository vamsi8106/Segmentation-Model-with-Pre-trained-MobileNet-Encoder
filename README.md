# Segmentation Model with Pre-trained MobileNet Encoder

## Introduction
This repository contains code for training a segmentation model using a pre-trained MobileNet encoder on the ISIC 2016 dataset. The objective is to design a custom decoder that predicts segmented masks for the given dataset. The dataset consists of 900 training images with corresponding masks, and 379 test images with masks. 

## Dataset Pre-processing and Custom Dataloader
- The images are resized to 128x128 during pre-processing.
- Custom dataloaders are implemented to load the dataset efficiently.

## Experiments
### Experiment 1: Feature Extraction
- Utilize a pre-trained MobileNet encoder trained on ImageNetV1.
- Design a custom decoder atop the encoder for the segmentation task.
- Train the decoder while keeping the encoder frozen.
- Options to take input for the decoder from the last layer of the encoder or from multiple layers are explored for potentially better results.

### Experiment 2: Fine-tuning
- Keep the same architecture as in Experiment 1.
- Train the segmentation model while fine-tuning encoder weights.

## Tasks
Perform the following tasks for both experiments:

1. **Intersection over Union (IoU) and Dice Score:** Calculate and report IoU and Dice score.
2. **Loss Plots:** Plot training and validation/testing loss curves.
3. **Results Analysis:** Analyze the results and provide observations.
4. **Visualization:** Visualize several samples alongside their generated masks and ground truth.
5. **Comparative Analysis:** Conduct a comparative analysis for both experiments.

## How to Use
1. Clone this repository.
2. Download the ISIC 2016 dataset and place it in the `data/` directory.
4. Run the `main.ipynb` files to train the segmentation models.
