# 👁️ Ocular Disease Detection and Classification

**Best Model:** EfficientNetB7 — **87.88% Test Accuracy**  
(Also includes ResNet50, MobileNetV3, DenseNet121 for comparison)

---

## 📂 Dataset

- **Source:** Kaggle or private dataset of ocular disease images (sources listed in `dataset_source.txt`)  
- **Splitting:** Stratified train/validation/test splits

---

## 🚀 Live Demo on Kaggle

Run the trained model on Kaggle GPU without any local setup:

- GPU used: **T4 ×2**  
- Results available in just a few minutes

---

## 📝 Step-by-Step Instructions

1. Go to [Kaggle](https://www.kaggle.com) → **New Notebook**  
2. Settings → Accelerator → **GPU T4 ×2**  
3. Add dataset to the notebook  
4. Upload the pre-trained model file:  
   - EfficientNetB7: `best_effnetb7_model.pth`  
   - ResNet50: `best_resnet50_model.pth`  
   - MobileNetV3: `best_mobilenetv3_model.pth`  
   - DenseNet121: `best_densenet121_model.pth`  
5. Copy and run the code from `Testing-Unseen Data/testing.ipynb`  
6. Update the model path in the notebook to your uploaded file  
7. Run inference on any unseen test image → outputs include **predictions + Grad-CAM visualizations**

---

## 🧪 Model Training & Evaluation

Training and validation for each model is organized in their respective notebooks:

- **EfficientNetB7:** `EfficientnetB7/EfficientNetB7_Notebook.ipynb`  
- **MobileNetV3 & DenseNet121:** `MobileNetV3 & Densenet121/MobileNetV3_DenseNet121_Notebook.ipynb`  
- **ResNet50:** `ResNet50/ResNet50_Notebook.ipynb` (includes Grad-CAM)  

**Evaluation:**  
- Testing on unseen data is in `Testing-Unseen Data/testing.ipynb`  
- Outputs include:  
  - Predictions for unseen images  
  - Grad-CAM visualizations highlighting model attention  
  - Accuracy, Precision, Recall, F1-score  
  - Confusion matrix & classification report  

---

## 🔍 Grad-CAM Model Interpretability

- Helps visualize which regions of the eye images the model focuses on  
- Correct predictions → attention on disease-relevant regions  
- Misclassifications → diffuse or incorrect attention  

---

## 📊 Key Results (Test Set)

| Model           | Accuracy | Precision | Recall | F1-Score |
|-----------------|---------|-----------|--------|----------|
| EfficientNetB7  | 87.88%  | 88.14     | 87.88  | 87.97    |
| ResNet50        | 85.05%  | 85.42     | 85.05  | 85.16    |

---

## 🔑 Takeaways

- Transfer learning on large CNNs (EfficientNet, ResNet, DenseNet) provides strong performance for ocular disease classification  
- Grad-CAM interpretability ensures model predictions focus on clinically relevant regions  
- Kaggle GPU (T4 ×2) is sufficient for training, validation, and inference  

---

Happy detecting! 👁️✨
