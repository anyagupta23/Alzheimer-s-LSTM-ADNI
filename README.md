# Alzheimer-s-LSTM-ADNI
This project explores the use of generative AI through LSTM to predict future stages of Alzheimer's disease.

# Predicting Alzheimer's Disease Progression Using LSTM Models on 3D MRI Sequences

**Contributors**  
Anya Gupta - [anyagupta25@mittymonarch.com](mailto:anyagupta25@mittymonarch.com)  
Kuan-Chuen Wu, PhD - [kuanchuenwu@@alumni.stanford.edu](mailto:kuanchuenwu@@alumni.stanford.edu)  

---

## Project Overview

This project uses a Long Short-Term Memory (LSTM) model to predict the progression of Alzheimer's disease based on sequences of 3D MRI scans. The goal is to forecast the next MRI image in a patient's sequence to visualize how Alzheimer's progresses, which can help clinicians in decision-making for treatment.

The **Jupyter notebook** included in this repository covers data preprocessing, model creation, training, and testing. It implements the LSTM architecture to analyze temporal MRI data from the Alzheimer's Disease Neuroimaging Initiative (ADNI) dataset.

---

## ADNI Dataset

The **Alzheimer's Disease Neuroimaging Initiative (ADNI)** dataset is a public dataset that provides access to 3D MRI brain scans. It contains longitudinal data, meaning multiple scans of the same patient over time. For this project, we focus on 99 patients, each with a sequence of four 3D T1-weighted MRI brain scans taken six months apart.

### Key Features:
- **3D MRI Images**: High-resolution scans showing structural changes in the brain.
- **Time Sequences**: Each patient has multiple images, allowing us to track the progression of Alzheimer's.
- **Labels**: Each scan is associated with Alzheimer's disease progression, providing essential data for predictive modeling.

For this project, the MRI images were preprocessed by converting 3D scans into 2D slices (middle slice, index = 96) and resizing them from 256x256 to 128x128 pixels to reduce computational load.

---

## Notebook Structure

The **Jupyter notebook** walks through the following steps:

1. **Preprocessing the Data**:
   - Load MRI images from the ADNI dataset.
   - Slice the 3D images to get 2D slices (for easier processing).
   - Resize the images and normalize the pixel values.

2. **Building the LSTM Model**:
   - Define a Sequential LSTM model in Keras.
   - The model takes a sequence of 3 input images and predicts the fourth one.
   - Include Dense layers to output a 128x128 image.

3. **Training the Model**:
   - Split the dataset into training (80%) and test (20%) sets.
   - Train the model over multiple epochs, saving progress with checkpointing.
   - Apply data augmentation techniques to enhance model generalization.

4. **Making Predictions**:
   - Use the trained LSTM model to predict the next image in a sequence.
   - Visualize the predicted and actual MRI slices to evaluate model performance.

---

## How to Run the Notebook

1. **Clone the repository**:
   ```bash
   git clone https://github.com/anyagupta23/Alzheimer-s-LSTM-ADNI.git
