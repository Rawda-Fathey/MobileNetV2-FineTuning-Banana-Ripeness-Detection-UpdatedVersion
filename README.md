# Banana Ripeness Detection 

A lightweight deep learning model to classify banana ripeness into four stages using a fine-tuned MobileNetV2 model.

## Overview

This project uses transfer learning with MobileNetV2 to classify bananas into:

- Unripe
- Partially Ripe
- Ripe
- Overripe

The model achieves **~92% accuracy** and is optimized for real-time inference, making it suitable for mobile and edge deployment.

---

## Model Details

- Architecture: MobileNetV2 (ImageNet pretrained)
- Input Size: 224 × 224 RGB images
- Optimizer: Adam (learning rate = 5e-5)
- Loss Function: Categorical Crossentropy
- Batch Size: 32
- Epochs: 50 (Early Stopping enabled)

Fine-tuning was applied to the last 30 layers of the base model.

---

## Dataset

The dataset consists of real and synthetic banana images:

- 2,400 real images (600 per class)
- 1,200 synthetic images
- Augmented training set (~12,000 images total)
- Image size: 224 × 224
The dataset is available here:  
🔗 [Banana Ripeness Dataset on GitHub](https://github.com/luischuquim/BananaRipeness)

Data augmentation techniques include rotation, zoom, shift, brightness adjustment, flipping, and shear transformations.

---

## Results

- Accuracy: 92%
- Macro F1-score: 0.91
- Inference Time: ~8.2 ms per image
- FLOPs: 0.56 GFLOPS

The model performs well across all four classes with balanced precision and recall.

---

## Tech Stack

- TensorFlow 2.x
- Keras
- Google Colab (Tesla T4 GPU)

---

## Use Cases

- Agricultural quality control
- Supply chain monitoring
- Smart farming applications
- Mobile-based fruit classification systems

---
