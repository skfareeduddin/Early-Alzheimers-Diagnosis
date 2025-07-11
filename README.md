
# 🧠 Early Alzheimer's Diagnosis Using Neural Networks

This project presents a deep learning approach for early diagnosis of Alzheimer's disease using MRI brain scans. Leveraging convolutional neural networks and transfer learning with ResNet50, the model classifies MRI images into four categories: **Non-Demented, Very Mild Demented, Mild Demented, and Moderate Demented**.

---

## 📰 Publication

📄 This project has been **published** in the *International Journal of Multidisciplinary Engineering in Current Research (IJMEC)* under the title:  
**“Early Alzheimer's Diagnosis Using Neural Networks”**

---

## 📂 Dataset

The dataset used is the **Augmented Alzheimer Dataset** sourced from Kaggle. It contains preprocessed MRI images categorized into:

- Non-Demented
- Very Mild Demented
- Mild Demented
- Moderate Demented

Directory structure:
```
AugmentedAlzheimerDataset/
├── MildDemented/
├── ModerateDemented/
├── NonDemented/
└── VeryMildDemented/
```

---

## 🧪 Key Features

- **Transfer Learning** using ResNet50
- Data Preprocessing with `ImageDataGenerator`
- **Visualization** of predictions and misclassifications
- **Callbacks** like EarlyStopping, ModelCheckpoint
- Performance evaluation using:
  - Accuracy & Loss plots
  - Confusion Matrix
  - ROC Curves
  - Classification Report

---

## 🛠️ Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/early-alzheimers-diagnosis.git
cd early-alzheimers-diagnosis
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Ensure your dataset is placed in:
```
/path/to/AugmentedAlzheimerDataset/
```

4. Update the dataset path in the script if necessary:
```python
train_dir = r'C:\path\to\AugmentedAlzheimerDataset'
```

---

## 🧠 Model Architecture

- **Base Model:** ResNet50 (pre-trained on ImageNet, with top layers removed)
- **Custom Layers:** Flatten → BatchNorm → Dense(2048) → Dense(1024) → Output(4)
- **Activation Functions:** ReLU, Softmax (for classification)

---

## 🚀 Training

- Epochs: 10  
- Batch Size: 16  
- Loss Function: `categorical_crossentropy`  
- Optimizer: `adam`

---

## 📈 Results

- Model trained with ~90%+ validation accuracy
- Visualizations include:
  - Accuracy/Loss graphs
  - Confusion Matrix
  - ROC Curves
  - Sample predictions with labels

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision, Recall, F1-score**
- **AUC-ROC per class**
- **Visualized performance over time**

---

## 📸 Sample Predictions

Correct and incorrect classifications are displayed with color-coded titles.

---

## 💡 Future Improvements

- Explore 3D MRI scans for temporal analysis  
- Integrate attention mechanisms for interpretability  
- Deploy as a web app for clinical demo  

---

## 👨‍💻 Author

**Syed Khaja Fareeduddin**  
Published in IJMEC | Deep Learning Enthusiast

---

## ⭐ If you found this useful

Please ⭐ star the repository and feel free to fork or contribute!
