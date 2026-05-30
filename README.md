# Glass vs Plastic Items Classification

## Project Overview

This project is a binary image classification system developed using deep learning. The objective is to classify item images into two categories: glass items and plastic items.

The project was implemented using Python in Google Colab. A Convolutional Neural Network model was trained from scratch, and a MobileNetV2 transfer learning model was also used for comparison. The fine-tuned MobileNetV2 model achieved the best performance.

## Student Information

Student ID: 22F23626  
Student Name: Shahla Suliman Alaamri  
Module: Artificial Intelligence and Deep Learning  
Platform: Google Colab  

## Dataset

The dataset was created using image URLs extracted from a Kaggle notebook titled Glass vs Plastic Items Image Classification. Images were downloaded into two folders:

- glass
- plastic

The final dataset contained:

- Glass images: 74
- Plastic images: 69
- Total images: 143

The dataset was split into training and validation sets using ImageDataGenerator.

## Tools and Libraries Used

- Python
- Google Colab
- TensorFlow
- Keras
- MobileNetV2
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- PIL
- Kaggle API

## Methodology

The project followed these steps:

1. Pull the Kaggle notebook into Google Colab.
2. Extract glass and plastic image URLs from the notebook.
3. Download valid images into class folders.
4. Display sample images from the dataset.
5. Resize images to 224 × 224 pixels.
6. Apply preprocessing and data augmentation.
7. Train a CNN model from scratch.
8. Train a MobileNetV2 transfer learning model.
9. Fine-tune the MobileNetV2 model.
10. Compare model performance using accuracy, loss, classification report, and confusion matrix.

## Models Used

### CNN from Scratch

A custom CNN model was built using convolutional layers, max pooling layers, dropout, and a sigmoid output layer for binary classification.

### MobileNetV2

MobileNetV2 was used as a pre-trained transfer learning model with ImageNet weights. The model was first trained with frozen base layers, then fine-tuned by unfreezing the last layers.

## Results

| Model | Validation Loss | Validation Accuracy |
|---|---:|---:|
| CNN from Scratch | 0.6896 | 48.15% |
| MobileNetV2 | 0.6225 | 70.37% |
| Fine-tuned MobileNetV2 | 0.5768 | 74.07% |

The fine-tuned MobileNetV2 model achieved the best performance.

## Evaluation Metrics

The models were evaluated using:

- Validation accuracy
- Validation loss
- Precision
- Recall
- F1-score
- Confusion matrix

## Conclusion

This project successfully applied deep learning to classify glass and plastic item images. The CNN model performed weakly because the dataset was small, while the fine-tuned MobileNetV2 model performed better due to transfer learning. The final result shows that transfer learning is more effective than training a CNN from scratch when the available dataset is limited.

Future improvements could include collecting more images, cleaning mislabeled samples, and testing other pre-trained models such as EfficientNet or ResNet.
