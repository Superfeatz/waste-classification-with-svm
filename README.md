# Waste Classification with SVM

This repository contains a project focused on waste classification using Support Vector Machines (SVM). The project involves data preprocessing, model training with different SVM kernels, and evaluating the performance of the models. Below are the details and instructions on how to set up and run the project.

## Dataset

The dataset used for this project can be downloaded from [Kaggle](https://www.kaggle.com/datasets/techsash/waste-classification-data/data).

## Project Structure

- `README.md`: This file, providing an overview and instructions for the project.
- `linearmodel.p`: Serialized linear SVM model.
- `polymodel.p`: Serialized polynomial SVM model.
- `rbfmodel.p`: Serialized RBF kernel SVM model.
- `svm.ipynb`: Jupyter Notebook containing the code for data preprocessing, model training, and evaluation.
- `svm.py`: Python script containing the code for data preprocessing, model training, and evaluation.

## Setup

1. **Install Dependencies**: Ensure you have the required libraries installed. You can use the following commands to install them:
   ```bash
   pip install -r requirements.txt
   ```

2. **Download Dataset**: Download the dataset from the provided Kaggle link and unzip it into the project directory.

3. **Run Jupyter Notebook**: Open and run the `svm.ipynb` notebook to execute the entire workflow, from data preprocessing to model evaluation.

## Usage

### Data Preprocessing

The data preprocessing steps include resizing images and removing corrupted files. This is done using the following functions:
- `resize_images(directory, output_size)`: Resizes images to the specified output size.
- `remove_unidentifiable_images(directory)`: Removes images that cannot be identified as valid images.

### Model Training

The SVM models are trained using different kernels: Linear, Polynomial, RBF, and Sigmoid. The training and evaluation are done using the `scikit-learn` library. The following models are trained and saved:
- `Linear Kernel SVM`
- `Polynomial Kernel SVM`
- `RBF Kernel SVM`
- `Sigmoid Kernel SVM`

### Model Evaluation

The trained models are evaluated using accuracy scores and classification reports. Confusion matrices are also generated to visualize the performance of each model.

### Model Testing

The saved models can be loaded and used to make predictions on new images. The `img2vec` library is used to extract features from images for prediction.

## Results

The accuracy of each model is printed, and confusion matrices are plotted to show the performance. Classification reports provide detailed metrics for each model.

## Contribution

Feel free to fork this repository and contribute by submitting pull requests. For major changes, please open an issue to discuss what you would like to change.
