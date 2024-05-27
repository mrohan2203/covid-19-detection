## COVID-19 Detection from CT scans

## Objective
The objective of this project is to develop a convolutional neural network (CNN) model to detect COVID-19 infections from chest CT scans. This model aims to assist healthcare professionals in quickly and accurately diagnosing COVID-19, thereby facilitating timely treatment and containment efforts.

## Data Collection
The dataset used for this project consists of two folders: one containing CT scans of patients diagnosed with COVID-19 and another containing CT scans of patients without COVID-19. The images were collected from publicly available medical repositories and are pre-labeled accordingly.<br>
Dataset link: https://www.kaggle.com/datasets/plameneduardo/sarscov2-ctscan-dataset    

## Data Preprocessing
The images were loaded and preprocessed by resizing them to a uniform size (224x224 pixels) and normalizing the pixel values to a range of [0, 1]. Data augmentation techniques, such as rotation, translation, zoom, and horizontal flipping, were applied to increase the variability and size of the training dataset, enhancing the model's generalization capabilities.

## Model Development
A transfer learning approach was used to build the model. The pre-trained VGG16 model, which has been trained on the ImageNet dataset, was used as the base model. Custom layers, including a global average pooling layer, dense layers, and a dropout layer, were added on top of the base model to adapt it for the binary classification task (COVID-19 vs. Non-COVID).

## Model Training
The model was compiled using the Adam optimizer and binary cross-entropy loss function. It was trained on the augmented training data for 20 epochs, with validation data used to monitor the model's performance and prevent overfitting.

## Model Evaluation
The model's performance was evaluated on a separate validation set, achieving a high accuracy in distinguishing between COVID-19 and Non-COVID CT scans. Metrics such as accuracy, precision, recall, F1-score, and ROC-AUC were used to assess the model's effectiveness.

## Conclusion
The trained model demonstrated strong performance in detecting COVID-19 from chest CT scans, showing potential as a valuable tool in the early diagnosis and treatment of the disease. The use of transfer learning and data augmentation significantly contributed to the model's robustness and accuracy.

## Future Work
Future improvements could include testing the model on larger and more diverse datasets, exploring additional augmentation techniques, and integrating the model into a user-friendly application for real-world deployment.

