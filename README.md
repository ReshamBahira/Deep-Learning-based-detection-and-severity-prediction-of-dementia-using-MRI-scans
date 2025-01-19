# Deep-Learning-based-detection-and-severity-prediction-of-dementia-using-MRI-scans
Dementia impacts millions globally, with cases rising. This study uses CNNs to classify dementia severity (no, very mild, mild, moderate) via MRI scans and Grad-CAM to highlight affected brain regions. This interpretable approach aids diagnosis, enhances understanding of progression, and boosts confidence in predictions.

Project Overview and Goals
Millions of individuals worldwide suffer from dementia, including Alzheimer's, and the number of cases is predicted to rise. Effective intervention requires accurate and timely diagnosis. However, conventional approaches frequently use simple deep learning or machine learning models to categorize or forecast dementia, which are unable to pinpoint the precise brain regions impacted or provide an explanation for their conclusions.

This study overcomes these constraints by employing Grad-CAM for visual explanations and CNNs for classification, making it particularly helpful for medical imaging.

Objectives
Use Deep Learning concepts like CNNs and Grad-CAM to detect and predict the severity of dementia using MRI scans.
Classify dementia into four classes:
Class 0: No Dementia
Class 1: Very Mild Demented
Class 2: Mild Demented
Class 3: Moderately Demented
Offer region-specific analysis by identifying key brain regions influencing predictions.
Improve confidence in model predictions and enhance interpretability.
Importance of Grad-CAM in Medical Diagnosis
In modern medicine, medical imaging technologies such as MRI provide useful diagnostic information. AI technologies based on deep learning architectures have shown remarkable results in analyzing medical images. However, the "black-box" nature of deep neural networks limits their adoption in clinical settings.

Grad-CAM (Gradient-weighted Class Activation Mapping) addresses this limitation by generating heatmaps that explain classification results. These visualizations highlight the contribution of input features to predictions, helping medical professionals trust and interpret the models' decisions.

Dataset Summary and Visualizations
Source
Dataset Origin: tps://www.kaggle.com/datasets/matthewhema/mri-dementia- augmentation-no-data-leak/data
Dataset Details
Original Dataset Size: 6,400 MRI images categorized into four dementia severity classes:
Mild Demented
Moderate Demented
Non-Demented
Very Mild Demented
Augmentation: Deep Convolutional GAN (DCGAN) increased the dataset to 6,400 balanced images (400 per class).
Methods
Model Architecture
Base Model: Convolutional Neural Network (CNN) with convolutional layers, pooling, batch normalization, and dropout regularization.
Additional Architectures Tested:
ResNet
DenseNet
InceptionV3
EfficientNet
Data Augmentation
DCGAN was used to generate synthetic MRI images to address class imbalance while preserving critical spatial features for classification.
Grad-CAM Visualization
Grad-CAM heatmaps highlight areas in MRI scans influencing model predictions, providing transparency and interpretability.
Evaluation Metrics
Accuracy
Precision (Macro Average)
Recall (Macro Average)
F1-Score (Macro Average)
Results
Performance Metrics
Model	Precision	Recall	F1-Score	Accuracy
CNN	0.87	0.87	0.87	0.87
ResNet	0.49	0.49	0.49	0.49
DenseNet	0.55	0.55	0.55	0.55
InceptionV3	0.57	0.57	0.56	0.57
EfficientNet	0.15	0.28	0.16	0.28
Observations
Best Model: CNN achieved the highest accuracy (87%) and minimal overfitting.
Confusion Matrix: CNN classified the "Very Mild Demented" class most accurately.
Grad-CAM Results
Grad-CAM heatmaps visualize brain regions influencing dementia severity predictions.
Example:
Very Mild Demented Image: Blue areas highlight influential regions.
Non-Demented Image: Red areas indicate minimal influence.
These results aid clinicians in further analysis and disease investigation.
(Include Grad-CAM visualizations here)

Training and Validation Observations
Models like CNN and DenseNet demonstrated strong performance with minimal gaps between training and validation accuracies, indicating balanced learning.
EfficientNet and ResNet struggled with generalization, showing signs of underfitting or overfitting.
Challenges
Class Imbalance: Addressed using DCGAN for augmentation.
Resource Constraints: Initial lack of powerful GPUs slowed dataset expansion, later resolved with Azure ML support.
Achievements
Achieved 87% accuracy on classifying dementia into four severity levels.
Successfully implemented Grad-CAM for model interpretability and clinical relevance.
Balanced the dataset using DCGAN, improving generalization.
Developed a generalized model with minimal overfitting or underfitting.
Future Work
Explore other augmentation techniques, such as StyleGAN, for further improvements.
Use multimodal approaches by integrating non-image data (e.g., patient history) with image data for better predictions.
Expand the model to predict other neurodegenerative diseases, such as Parkinson's or Huntington's.
Citations
ScienceDirect Article 1
ScienceDirect Article 2
Nature Article
MDPI Article
IEEE Article
Authors
Resham Bahira
Kulveen Kaur
Nithin Kumar H G
Sudhanshu Pawar
