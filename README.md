🧿  # Eye Disease Recognition using Deep Learning

📌 Overview
This project focuses on the automated detection of eye diseases using deep learning techniques applied to fundus images. The manual diagnosis of ocular conditions is prone to human error and can be time-consuming, which necessitates the development of intelligent systems to assist clinicians.

We implemented and compared multiple deep learning models — VGG-19, ResNet50, and Vision Transformer — on the ODIR dataset to classify fundus images into healthy or diseased categories. To enhance model performance, Local Binary Pattern (LBP) transformations were applied for texture-based feature extraction.



🎯 Objectives
Automate the detection of common eye diseases from fundus images.

Improve diagnostic accuracy using deep learning.

Handle dataset imbalance and enhance image quality using preprocessing and augmentation techniques.

Compare the performance of multiple architectures.


🧠 Models Used
VGG-19: A deep CNN model known for capturing hierarchical visual features.

ResNet50: A residual learning network that addresses vanishing gradients in deep architectures.

Vision Transformer (ViT): Applies transformer-based mechanisms to vision tasks by treating image patches as sequences.


🧪 Dataset
ODIR Dataset

Total: 6,000+ fundus images

Classes: 8 categories including normal, diabetic retinopathy, glaucoma, etc.

Due to class imbalance, the task was converted into binary classification (Healthy vs Diseased).

⚙️ Preprocessing & Feature Extraction
Background Removal: Manual background cleaning to isolate the fundus.

Grayscale Conversion: To simplify features and reduce dimensionality.

Local Binary Pattern (LBP): Used to extract texture-based features, improving classification in some models.


📊 Results
Model	Accuracy	Validation Loss
VGG-19	High	Moderate
ResNet50	100%	0.004
Vision Transformer	Low	High

ResNet50 with LBP performed best with minimal validation loss.

ViT underperformed, indicating it might require more training data or different tuning.


✅ Conclusion
This project successfully demonstrated that deep learning models can be effectively used to detect eye diseases from fundus images. The best-performing model was ResNet50 with LBP-enhanced inputs. Future enhancements could include:

Using GANs to synthetically balance the dataset

Experimenting with more advanced vision models or ensembles

Incorporating clinical metadata for multimodal analysis

📁 Project Structure
bash
Copy
Edit
📦 Eye-Disease-Recognition/
├── data/
│   └── ODIR/                  # Fundus image dataset
├── models/
│   ├── resnet50_model.py
│   ├── vgg19_model.py
│   └── vit_model.py
├── preprocessing/
│   └── lbp_transform.py
├── results/
│   └── accuracy_plots.png
├── main.py                    # Main training/testing script
└── README.md                  # Project overview
👩‍⚕️ Future Scope
Integration into medical diagnostic tools for real-time use.

Extend classification to multi-label (detect multiple diseases in one image).

Combine with patient history for predictive analytics.
