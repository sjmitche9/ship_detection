# Ship Detection in Satellite Imagery Using CNN and ANN

This project explores object detection—specifically identifying ships in satellite imagery—using convolutional neural networks (CNNs) and artificial neural networks (ANNs).

## 📷 Dataset

- **Source**: Planet satellite imagery from California
- **Images**: 4,000 RGB images (80x80 pixels)
- **Labels**: Binary — `"ship"` (1,000 images) and `"no-ship"` (3,000 images)
- **Resolution**: 3-meter spatial resolution (RGB only)

"No-ship" images include:
- Land
- Water
- Partial ships
- False positives from previous models

## 🚀 Model Architecture

The neural network consists of 5 layers:

1. **Convolutional Layer**
   - 32 filters
   - 3x3 kernel
   - Activation: ReLU

2. **Max Pooling Layer**
   - Pool size: 2x2
   - Helps reduce overfitting and dimensionality

3. **Flatten Layer**
   - Converts 2D input to a 1D vector

4. **Dense Layer**
   - Activation: ReLU

5. **Output Layer**
   - 2 neurons
   - Activation: Sigmoid
   - Threshold: ≥ 0.5 = Ship, < 0.5 = No-ship

## 🛠️ Preprocessing

- Normalize pixel values to [0, 1] by dividing by 255
- Split: 70% training / 30% testing

## ⚙️ Training Configuration

- **Epochs**: 10  
- **Batch Size**: 200  
- **Optimizer**: Adam  
- **Loss Function**: Binary Cross Entropy

## ✅ Results

- **Test Accuracy**: 95.3%
- **Test Loss**: 0.124

These results are strong for a baseline model, highlighting the potential for applying deep learning in remote sensing tasks.

## 📌 Motivation

- Monitor ship traffic in restricted zones
- Detect illegal fishing and unauthorized marine activity
- Leverage satellite data for large-scale maritime surveillance

## 🔗 Code

Repository: [sjmitche9/ship_detection](https://github.com/sjmitche9/ship_detection)

## 📚 References

1. [Appsilon – Deep Learning in Satellite Imagery](https://appsilon.com/deep-learning-in-satellite-imagery/)
2. [Kaggle Dataset – Ships in Satellite Imagery](https://kaggle.com/rhammell/ships-in-satellite-imagery)
3. [DeepAI – Max Pooling](https://deepai.org/machine-learning-glossary-and-terms/max-pooling)

---

