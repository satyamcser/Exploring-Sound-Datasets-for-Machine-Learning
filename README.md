# Exploring-Sound-Datasets-for-Machine-Learning

# Colab: https://colab.research.google.com/drive/1eYlRrU3KjWyXdGryo4saMGqVh2fEhUy7?usp=sharing

Background:
This work explores the use of machine learning techniques to classify sounds from the UrbanSound8K dataset. This dataset contains 8732 labeled sound excerpts of 10 urban sound categories like car horns, gun shots, jackhammers etc.

The goal is to use this dataset to train machine learning models to accurately classify urban sounds.

Data Analysis:
The paper first loads the dataset and analyzes the distribution of samples across categories. It finds that most categories have 1000 samples except car horns, gun shots and sirens.

It then analyzes audio features like length, bitrate, channels, sample rate across all samples to characterize the diversity of recordings. It finds that while the recordings vary a lot in their raw characteristics, the samples from each class have consistent average feature values.

The paper then visualizes the waveforms, spectrograms and MFCC features for sample recordings from each class. This helps understand the variability across classes.

Feature Extraction:
The paper settles on using Mel Frequency Cepstral Coefficients (MFCCs) as the input features for classification instead of waveforms or spectrograms. MFCCs provide a compact representation capturing only the most useful frequency information to discriminate sounds.

40-D MFCC vectors are extracted for 3-4 sec long recordings and padded to get fixed length inputs for the neural network.

Model Building:
The paper experiments with various Convolutional Neural Network architectures using Conv2D and MaxPooling2D layers. Dropout regularization and Adam optimizer are used to prevent overfitting.


The final model achieves 90.5% accuracy on a held-out test set, demonstrating effective learning from raw audio signals using deep CNNs.

Conclusion:
The project shows how deep learning can allow discrimination between urban sounds with high accuracy. It also discusses ways to further improve performance using other input features, network architectures and more training data.

The hands-on experience would be valuable for audio classification tasks using machine learning.

# By- Satyam Mishra
