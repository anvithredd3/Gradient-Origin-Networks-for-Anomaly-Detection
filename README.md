# Gradient Origin Networks (GON) for Anomaly Detection

This repository contains code, notebooks, and documentation related to Gradient Origin Networks (GON), a novel approach to implicit generative modeling and anomaly detection. The project builds upon the concepts introduced in the original GON paper, which was accepted at ICLR 2021.

## Project Overview

Gradient Origin Networks (GON) introduce a streamlined architecture that eliminates the need for separate encoding networks by utilizing gradients for encoding, thereby reducing overall model complexity and computational costs. The primary focus of this project is on anomaly detection, where the GON is used to identify data points that significantly deviate from expected patterns.

### Original Paper Details

The original GON paper proposes a new type of generative model that can quickly learn a latent representation without an encoder. This is achieved using empirical Bayes to calculate the expectation of the posterior, implemented by initializing a latent vector with zeros, then using the gradient of the log-likelihood of the data with respect to this zero vector as new latent points. The approach shares characteristics with autoencoders but with a simpler architecture, as demonstrated in a variational autoencoder equivalent that permits sampling.

- **Citation:**

  ```
  @inproceedings{bond2020gradient,
     title     = {Gradient Origin Networks},
     author    = {Sam Bond-Taylor and Chris G. Willcocks},
     booktitle = {International Conference on Learning Representations},
     year      = {2021},
     url       = {https://openreview.net/pdf?id=0O_cQfw6uEh}
  }
  ```

- **Authors:** Sam Bond-Taylor, Chris G. Willcocks
- **Paper Link:** [Gradient Origin Networks - ICLR 2021](https://openreview.net/pdf?id=0O_cQfw6uEh)
- **Project Page:** [cwkx.github.io/data/GON/](https://cwkx.github.io/data/GON/)

## Contents


## Key Features

- **GON Architecture:** A single network for both encoding and decoding, with latent vectors initialized at zero and gradients used for encoding.
- **Anomaly Detection:** Implementation of a dynamic threshold-based anomaly detection system using reconstruction losses.
- **Datasets:** Experiments conducted on MNIST (including corrupted MNIST) and MVTec AD datasets to demonstrate the effectiveness of GON.
- **Comparison:** Results compared with traditional Autoencoder models in terms of performance, reconstruction errors, and confusion matrices.

## Usage

Each notebook contains detailed comments and explanations of the code. You can run the notebooks to replicate the experiments or adapt the code for similar tasks.


- **Notebooks:**
  - `autoencoder-mnist.ipynb`: Implementation of an Autoencoder for anomaly detection on the MNIST dataset.
  - `FINAL_FINAL_AUTOEN_MVTECH.ipynb`: Final version of the Autoencoder for the MVTec AD dataset.
  - `GON_MNIST.ipynb`: Gradient Origin Networks implementation for the MNIST dataset.
  - `GON_MVTEC.ipynb`: Gradient Origin Networks implementation for the MVTec AD dataset.
  - `GON_Decoder_for_Tiny_Datasets.ipynb`: Exploring the GON decoder's performance on tiny datasets using optimal transport techniques.
  - `Gradient_Origin_Networks.ipynb`: Core notebook detailing the methodology and implementation of GON for various tasks.


## Results

The results section in the notebooks provides an in-depth analysis of the GON's performance on different datasets, including loss curves, confusion matrices, and the comparison of GON with Autoencoder models.

## Additional Work

The project also explores the use of optimal transport techniques, such as Sinkhorn divergence, to enhance the generative performance of GON on small datasets.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

The original Gradient Origin Networks (GON) paper was authored by Sam Bond-Taylor and Chris G. Willcocks and was accepted at ICLR 2021. The implementation in this repository builds upon their work, adding further developments and experiments focused on anomaly detection.

## Contributors
- Anvith Reddy Nemali
- Sai Surya Vidul Chinthamaneni
---
