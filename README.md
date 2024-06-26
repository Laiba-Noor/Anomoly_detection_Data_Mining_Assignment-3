# Anomaly Detection Framework with Contrastive Learning and GAN

## Introduction
This repository contains an anomaly detection framework that leverages contrastive learning and Generative Adversarial Networks (GAN) to address overfitting in multivariate time series data. The implementation integrates various techniques, including data augmentation with geometric distribution masks, a Transformer-based Autoencoder, and contrastive loss, to achieve robust anomaly detection.

## Implementation Details

### Data Loading and Preprocessing
The framework begins by loading the dataset from Google Drive and preprocessing it using pandas DataFrames.
This step ensures that the data is ready for further processing and model training.

![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/2aa27c34-0fe3-431c-aee8-5484afd76ad2)


![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/0ae0e94d-2b48-4b06-ad18-0f911f7fc790)
### Data Visualization
![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/876967ff-b7db-4a97-8fd9-4505f24539aa)

![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/f6e472dd-d358-4fec-b573-4437bc801c0d)

### Geometric Masking
Geometric distribution masks are applied to the data as a data augmentation technique. This helps in introducing variability into the training data while preserving the underlying patterns.

![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/c5b27bc3-26ca-4db0-8ad9-d0c7efbc1f80)


### Transformer-based Autoencoder
A Transformer-based Autoencoder architecture is employed for feature extraction and reconstruction. This architecture consists of multi-head self-attention layers and feed-forward networks, which are effective in capturing temporal dependencies in time series data.


### Training
The Autoencoder model is trained using the preprocessed data. The training process involves minimizing the mean squared error between the input and reconstructed data. This step enables the model to learn meaningful representations of the input data.

![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/818bb1b9-041e-4b0e-81fc-77b1a6b4a2ae)


### Discriminator
A discriminator model is built to distinguish between real and reconstructed data samples. This model is trained alongside the Autoencoder as part of the GAN framework.

### GAN Model
The GAN model combines the Autoencoder and discriminator into a unified framework. It utilizes adversarial training to enhance the quality of the reconstructed data while simultaneously training the discriminator to distinguish between real and fake samples.

### Evaluation
The trained Autoencoder is evaluated on a separate test dataset to detect anomalies. Reconstruction errors are computed for each data sample, and anomalies are identified based on predefined thresholds.
![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/7c33b78b-9b97-4866-8d56-f1a89d7ab991)
![image](https://github.com/Laiba-Noor/Anomoly_detection_Data_Mining_Assignment-3/assets/88136283/17a0d7d4-a0ac-47ab-969d-bed030f47174)

## Useful Links
For your convenience, you can access public datasets for time series anomaly detection, such as the PSM dataset from eBay, using the following link: [TS-AD-Datasets](https://github.com/elisejiuqizhang/TS-AD-Datasets)

