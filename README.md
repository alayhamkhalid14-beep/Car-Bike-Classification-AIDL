# Automated Vehicle Type Classification for Intelligent Toll Systems

**Name:** Alayham Khalid Almalki
**Module:** Artificial Intelligence and Deep Learning (COMP 20037)

##  Project Overview
This project addresses the challenge of automated vehicle classification for Intelligent Transportation Systems (ITS). Specifically, it implements a binary image classification model to distinguish between **Cars** and **Bikes** using Deep Learning techniques.

##  Dataset
* **Source:** Custom dataset aggregated from Google Drive.
* **Total Images:** 1,361 images.
* **Classes:**
    * Car: 613 images
    * Bike: 748 images
* **Preprocessing:** Images resized to 224x224 pixels and normalized to range [0, 1].

##  Methodologies
We implemented and compared two distinct deep learning architectures:
1.  **Custom CNN:** A sequential Convolutional Neural Network designed from scratch.
    * *Features:* 3 Convolutional blocks, BatchNormalization, and Dropout (0.1) to reduce overfitting.
2.  **ResNet50:** A Transfer Learning model pre-trained on ImageNet (with frozen base layers).

##  Results
| Model | Validation Accuracy | F1-Score | Key Observation |
| :--- | :--- | :--- | :--- |
| **Custom CNN** | **89%** | **0.89** | Best performance; high balanced accuracy. |
| **ResNet50** | 75% | 0.73 | Lower accuracy; struggled to recall 'Car' class features. |

##  Conclusion
The study concludes that for this specific dataset size, the **Custom CNN** significantly outperformed the frozen ResNet50 model. The custom model successfully captured domain-specific features of vehicles, whereas the transfer learning model required further fine-tuning.

##  How to Run
1.  Open the `.ipynb` file in Google Colab.
2.  Upload the dataset folder to your Google Drive.
3.  Mount your Drive in Colab and update the `base_dir` path.
4.  Run all cells to reproduce the training and evaluation results.
