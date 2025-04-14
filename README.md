# Predicting-ASD-using-Eye-Tracking-Data-and-Deep-Learning

## Overview
This project explores the use of deep learning techniques to predict Autism Spectrum Disorder (ASD) using eye-tracking data. Various neural network architectures, including CNNs, LSTMs, and Transformers, are applied to analyze the data and improve classification accuracy. Our method aggregates multiple eye-tracking images per individual using sequence modeling techniques to enhance diagnostic reliability.

## Repository Structure
```
📂 Predicting-ASD-using-Eye-Tracking-Data-and-Deep-Learning
│── 📂 cnn_model/             # CNN-based model implementation
│── 📂 cnn_lstm_model/        # CNN + LSTM hybrid model
│── 📂 cnn_transformer_model/ # CNN + Transformer model
│── 📂 densenet_model/        # DenseNet model
│── 📂 resnet_model/          # ResNet model
│── 📂 vgg19_model/           # VGG19 model
│── 📂 preprocess/            # Data preprocessing scripts
│── 📂 results/               # Model evaluation results
│── 📜 ENPM703_Report.pdf     # Project report detailing methodology and findings
│── 📜 requirements.txt       # Dependencies and required libraries
│── 📜 README.md              # Project documentation (this file)
```

## Dataset
The dataset consists of eye-tracking data collected from 59 children (30 ASD and 29 neurotypical) and converted into RGB scanpath images. The dataset includes:
- **547 images** (219 ASD, 328 neurotypical)
- **Metadata files** mapping images to participants
- **Data stored in Figshare repository:** [Dataset Link](https://figshare.com/s/5d4f93395cc49d01e2bd)

The split and augmented dataset can be accessed from: https://drive.google.com/file/d/1EK1o4L-RIBF4Y_fLRnpdTs7kZqrJmSYZ/view?usp=sharing

Eye movements were recorded using the **SMI RED-m** remote eye-tracker while participants watched curated video stimuli. 

## Methods
We experimented with multiple deep learning models for ASD classification:
- **Custom CNN**: Three convolutional layers with max-pooling, reaching **76.24% accuracy, AUC 0.83**.
- **Transfer Learning (ResNet50, DenseNet121, VGG19)**:
  - Best results: **DenseNet - 79.21% accuracy, AUC 0.846**.
- **Voting-based baseline**: Aggregating multiple image predictions per participant (**AUC 0.90**).
- **LSTM-based sequence modeling**: Capturing temporal dependencies across images (**AUC 1.0** with attention mechanism).
- **Transformer-based model**: Achieved **88.89% accuracy, AUC 0.95**, highlighting its ability to generalize well.


## Results
- **Best model: Transformer-based approach (AUC 0.95, Accuracy 88.89%)**
- **Sequence modeling significantly improved individual-level classification.**
- **Increasing the number of images per participant improved prediction confidence.**

Detailed resuts and project report can be found ![here](ENPM703_Report.pdf)

## Limitations & Future Work
- **Dataset size**: Expanding beyond 59 participants would enhance generalizability.
- **Noise in eye-tracking data**: Outliers and inconsistencies can affect predictions.
- **Hardware dependency**: Eye-tracking equipment limits data collection.

### Future Directions:
- Expanding dataset diversity across age groups.
- Combining eye-tracking with speech or facial expression analysis.
- Exploring **Vision Transformers** and **self-supervised learning**.

## License
This project is licensed under the MIT License. Feel free to use and modify it as needed.

## Contributors
- [Suhas Nagaraj](https://github.com/suhasnagaraj99)
- [Swaraj Mundruppady Rao](https://github.com/SwarajMundruppadyRao)
- [Koustubh](https://github.com/koustubh1012)
- Arya Sunil Gangatkar

For any inquiries or issues, please open an issue on GitHub or contact the contributors.

