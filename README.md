#  Deep Learning for Scene Classification (CNN + Transfer Learning)

##  Overview

This project explores image classification using a custom CNN and transfer learning with pre-trained models. The goal is to compare performance, efficiency, and interpretability across different architectures.

---

##  Dataset

* Intel Image Classification Dataset
* 6 classes: Buildings, Forest, Glacier, Mountain, Sea, Street

---

##  Models Used

###  Baseline CNN

* Built from scratch
* Trained fully (21M parameters)

###  Transfer Learning Models

* ResNet50 (feature extraction)
* DenseNet121 (fine-tuned)
* EfficientNetB0 (fine-tuned)

---

##  Methodology

* Data Augmentation (Random Flip, Rotation, Normalization)
* Transfer Learning using ImageNet weights
* Partial Fine-Tuning (DenseNet121 & EfficientNetB0)
* Optimizer: Adam
* LR Scheduler: ReduceLROnPlateau

---

##  Results

| Model          | Accuracy   | Top-3 Acc | F1 Score   |
| -------------- | ---------- | --------- | ---------- |
| Baseline CNN   | 84.32%     | 98.48%    | 0.8422     |
| ResNet50       | 89.26%     | 99.33%    | 0.8917     |
| DenseNet121    | **92.49%** | 99.76%    | **0.9244** |
| EfficientNetB0 | 92.16%     | 99.76%    | 0.9211     |

---

##  Key Insights

* DenseNet121 achieved the best overall performance.
* EfficientNetB0 had the highest validation accuracy.
* ResNet50 performed efficiently with very few trainable parameters.
* Fine-tuning significantly improved performance.

---

##  Model Interpretability

Grad-CAM was applied on DenseNet121 to visualize important regions influencing predictions.

---

##  Performance Summary

| Model          | Trainable Params | Avg Epoch Time |
| -------------- | ---------------- | -------------- |
| ResNet50       | 526K             | 22.1s          |
| DenseNet121    | 2.42M            | 23.4s          |
| EfficientNetB0 | 3.48M            | 22.4s          |

---

##  Kaggle Notebook

👉 https://www.kaggle.com/code/farwairfan112/deep-learning-cnn-transfer-learning

---

##  Project Structure

```
├── data/
├── models/
├── notebooks/
│   └── training.ipynb
├── results/
│   ├── graphs/
│   ├── confusion_matrices/
│   └── gradcam/
├── README.md
```

---

##  Technologies Used

* Python
* PyTorch
* Torchvision
* Matplotlib
* Scikit-learn

---

##  Conclusion

DenseNet121 provided the best balance of accuracy and generalization, while EfficientNetB0 offered strong performance with efficient scaling. Transfer learning proved highly effective for this task.

---

##  Author

Farwa Irfan
