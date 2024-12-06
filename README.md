# Deep-Learning--GAN
Generating artifical anime faces
Objective

The project focuses on generating synthetic anime faces using a GAN, trained on a public dataset.

Dataset:

Anime Face Dataset from Kaggle: AnimeFaceDataset. Images preprocessed to 64x64 resolution with pixel values normalized to a range of [-1, 1]. Data loaded using PyTorch's ImageFolder and DataLoader.

Dataset URL: 'https://www.kaggle.com/datasets/splcher/animefacedataset'

Model Architecture:

Generator:

Takes a random latent tensor as input and generates 64x64 RGB images. Uses transposed convolution layers with ReLU activations and Batch Normalization. Final layer uses Tanh activation for outputs in the range [-1, 1].

Discriminator:

Classifies input images as real or fake using convolutional layers with Leaky ReLU and Batch Normalization. Outputs a probability score through a sigmoid layer.

Training Details:

Loss Functions:

Binary Cross-Entropy Loss for both generator and discriminator. Generator trained to fool the discriminator by maximizing its probability of generating "real" images. Optimization: Adam optimizer used with a learning rate of 0.0002.

Training Epochs:

Ran for 10 epochs with iterative updates to both networks. Saved intermediate outputs for visual inspection of the generator’s progress. Results:

Generated synthetic anime faces evolved significantly during training. Final model checkpoints saved for both generator (G_anime_faces.pth) and discriminator (D_anime_faces.pth).

Visualization:

Random latent tensors passed through the generator to produce and save sample outputs. A video created to visualize the progression of generated images across epochs.

Key Takeaways The GAN successfully generated anime faces by training the generator and discriminator in tandem. The project demonstrates effective application of GANs for synthetic image generation with consistent visual improvements over training epochs.
