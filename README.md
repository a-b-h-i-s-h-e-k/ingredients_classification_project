# Image_based_Ingredients_Classification

## Project Overview

This project aims to classify ingredients in food images using deep learning techniques. The dataset used includes 101,000 images spanning 101 different categories, supplemented by the Ingredients101 dataset that provides detailed ingredient information for each image. The project involves data preprocessing, training a convolutional neural network (CNN) using a pre-trained ResNet-50 model, and evaluating the model's performance.

## Contents
1. Libraries and Tools
2. Environment Setup and Data Acquisition
3. Data Preprocessing
4. Model Training and Validation
5. Inference and Evaluation
6. Results and Metrics
7. How to Run the Project

## Libraries and Tools
The following libraries and tools were used in this project:

- os: Interacts with the operating system.
- zipfile: Handles ZIP file operations.
- gdown: Downloads files from Google Drive.
- sys: Accesses system-specific parameters and functions.
- cv2 (OpenCV): Performs image processing tasks.
- numpy: Provides support for large multi-dimensional arrays and matrices.
- torch: The main package for PyTorch, a deep learning framework.
- torchvision: Provides datasets, models, and image transformations for PyTorch.
- pandas: Manages and analyzes data structures.
- matplotlib: Creates visualizations and plots.
- scikit-learn: Provides tools for data preprocessing and evaluation.
- tqdm: Displays progress bars for loops and data loading.
- collections: Enhances dictionaries with default values.

## Environment Setup and Data Acquisition
To set up the environment, ensure the necessary libraries are installed. The Kaggle API is used to download the food image dataset. Additionally, the Ingredients101 dataset is downloaded from Google Drive. Both datasets are then unzipped and prepared for further processing.

## Data Preprocessing
The preprocessing steps include:

- Reading and organizing ingredient data from text files.
- Binarizing the ingredient information using MultiLabelBinarizer to create a binary matrix format.
- Creating DataFrames for training, validation, and test sets by associating image paths with their corresponding class IDs.
- Saving the processed DataFrames to HDF5 files for efficient storage and retrieval.

## Model Training and Validation
The project employs a pre-trained ResNet-50 model, modified to fit the number of target classes. The training process involves:

- Setting up the DataLoader for efficient data handling.
- Defining the loss function and optimizer.
- Implementing a training loop that performs forward and backward propagation, computes loss, and updates model parameters.
- Evaluating the model on a validation set after each epoch and saving the best-performing model.

## Inference and Evaluation
For inference, the best-performing model is loaded, and predictions are made on the test dataset. The model's performance is evaluated using several metrics, including:

- F1 Score: Measures the balance between precision and recall.
- Precision and Recall: Evaluate the accuracy of the positive predictions.
- Hamming Score: Computes the average label-based accuracy for multi-label classification.

## Results and Metrics
The training and validation process includes plotting the loss and accuracy curves to visualize the model's performance. The evaluation metrics are printed to provide insights into the model's effectiveness.

## How to Run the Project
1. Set Up Environment: Install the required libraries by running pip install required_module.
2. Download and Prepare Data: Follow the steps in the "Environment Setup and Data Acquisition" section to download and unzip the datasets.
3. Run Training: Execute the training script to train the model on the dataset.
4. Run Inference: Use the inference script to evaluate the model on the test dataset and obtain performance metrics.