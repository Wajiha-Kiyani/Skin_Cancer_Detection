### **Skin Cancer Detection Model**
---
### **Overview**
This project focuses on classifying skin lesion images into benign or malignant categories using a pre-trained CNN model (**ResNet50**) with transfer learning. Below are the insights and requirements for the project.
---
### **Model Insights**
1. **Dataset Details**:
   - **Name**: Skin Cancer ISIC Dataset
   - **Structure**:
     - Training Images: 1,791
     - Validation Images: 448
     - Testing Images: 118
   - **Preprocessing**:
     - Images were resized to **224x224**.
     - Normalized pixel values to the range [0, 1].
2. **Model Architecture**:
   - **Base Model**: ResNet50 (pre-trained on ImageNet).
   - **Modifications**:
     - Final fully connected layer replaced with a dense layer for binary classification.
     - Applied transfer learning with fine-tuning.
3. **Evaluation Metrics**:
   - **Accuracy**: 14%
   - **Precision (macro)**: 2%
   - **Recall (macro)**: 11%
   - **F1-Score (macro)**: 3%
   - **Challenges**:
     - Imbalanced dataset impacted performance.
     - Warnings indicated poor predictions for certain labels.
4. **Recommendations**:
   - Augment data with advanced techniques (flipping, rotation, brightness).
   - Fine-tune more layers of ResNet50 to improve learning.
   - Explore other pre-trained models like EfficientNet.
   - Expand the dataset to improve class balance and generalization.
---
### **Requirements**
#### **1. Python Version**:
- Python 3.8 or above
#### **2. Libraries**:
Run the following commands to install the required libraries:
```bash
pip install kagglehub tensorflow scikit-learn numpy pillow matplotlib
```
#### **3. Dataset**:
- **Source**: Kaggle ("nodoubttome/skin-cancer9-classesisic")
- **Download Command**:
```python
import kagglehub
path = kagglehub.dataset_download("nodoubttome/skin-cancer9-classesisic")
print("Dataset downloaded to:", path)
```
#### **4. Hardware**:
- **Recommended**: GPU for faster training (NVIDIA GPU with CUDA support).
- Minimum 8GB RAM for processing.
---
### **How to Run**
1. Clone the repository.
2. Download the dataset using the provided script.
3. Follow the preprocessing, model training and evaluation steps as in file.
4. Visualize the evaluation metrics and confusion matrix.
---
### **Conclusion**
While the project demonstrated the potential of transfer learning, the results indicate the need for optimization. By addressing class imbalance and fine-tuning the model further, this framework can evolve into a robust solution for skin cancer detection.
***