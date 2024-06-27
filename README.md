# Speaker Identification

## Overview

This repository contains the code for a speaker identification project using the PTDB-TUG Dataset. The project is organized into three tasks, each implemented in a separate folder: `Task_1`, `Task_2`, and `Task_3`.

## Assignment Structure

### Task 1 - Data Preparation (Task_1)
- **Jupyter Notebook:** `task1.ipynb`
- **Spectrograms Dataset:** Located in the `Spectrograms/` folder
- **Description:** This task involves downloading the PTDB-TUG Dataset, exploring its structure, and creating spectrograms for each utterance.

### Task 2 - Baseline Speaker Identification (Task_2)
- **Model Code:** `Task2.ipynb`
- **Trained Model:** `voice.pth`
- **Description:** This task involves building a baseline Convolutional Neural Network (CNN) for speaker identification. Regularization techniques, such as batch normalization and dropout, are applied to prevent overfitting. The Adam optimizer with a weight decay of 1e-5 is used for optimization.

### Task 3 - Speaker Identification with Noisy Data (Task_3)
- **Model Code:** `Task3.ipynb`
- **Trained Model:** `voice_noise.pth`
- **Noise-added Dataset:** Created and stored in the `Spectrograms_noise/` folder
- **Description:** This task involves introducing noise to the audio files, subsequently creating new spectrograms. The modified dataset, named `Spectrograms_noise`, was utilized to train the model. Additionally, data augmentation techniques were applied to enhance model accuracy.

## Additional Files
- `requirements.txt`: Contains the required dependencies for running the project.
- `README.md`: Provides an overview of the project, instructions, and additional details.

## Additional Information

- The project uses PyTorch for model implementation and training.
- For Task 2 and Task 3 model training, the spectrogram datasets (Spectrograms and Spectrograms_noise) structure was modified by relocating the noise folders outside the main dataset directory. This adjustment enables the model to seamlessly read and recognize all nine speaker classes during the training process.

## Results

- Task 2 uses the spectrograms generated in Task 1 for training and evaluation.
- The models are saved with filenames `voice.pth` for Task 2 and `voice_noise.pth` for Task 3.

## Installation

To install the required dependencies, run:
```bash
pip install -r requirements.txt
```

## Usage

### Task 1: Data Preparation
1. Navigate to the `Task_1` folder.
2. Open and run `task1.ipynb` to generate spectrograms.

### Task 2: Baseline Speaker Identification
1. Navigate to the `Task_2` folder.
2. Open and run `Task2.ipynb` to train the baseline CNN model.

### Task 3: Speaker Identification with Noisy Data
1. Navigate to the `Task_3` folder.
2. Open and run `Task3.ipynb` to train the model with noisy data.

