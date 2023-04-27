# Evaluating the feasibility of using Generative Models to generate Chest X-Ray Data
Using GANs and Stable Diffusion to generate Chest Xray data points and evaluating them using convolutional classifiers.

This repository is the official implementation of [Evaluating the feasibility of using Generative Models to generate Chest X-Ray Data]

## How to run

- Open notebooks in the order mentioned below (preferably on colab, for ease of use due to formatting)
- Descriptions and instructions are provided in the notebooks

## Training

To train the models in the paper, open this notebook:

> [Chest XRay Image Synthesis](https://colab.research.google.com/drive/1YHHQAmv2mswfk6uo1-4zk6E8YfndxYpT?usp=sharing)
> The PGGAN is pre-trained and can only be used to generate samples, meanwhile the stable diffusion model is fine-tuned in the notebook and saved to huggingface.
> (Make a copy if you wish to make changes.)

## Data Generation and Evaluation

To generate the chest x-ray data and evaluate using a classifier, open this notebook:

> [Data Synthesis For Image Classification](https://colab.research.google.com/drive/11F7nu_SX8Oxp2s04-pKh3JAtCzsodhX7?usp=sharing)
> This notebook is used to genarate multiple images to be used as a dataset or in addition to a dataset.
> (make a copy if you wish to make changes)


## Pre-trained Models

You can download pretrained model here:

- [Model Checkpoints](https://drive.google.com/drive/u/0/folders/1qJgEFWvte6mDTQf1DKTXUDohsHZphrg_) trained on Chest Xray14 train set. (fine-tuned version of stable diffusion v2.1-512px)

> Use the data generation and evalutation notebook linked above to use any of these models yourself.

## Results

- Quantitative results:
    > Classifier trained on no finding chest x-rays vs Edema chest x-rays, first with only real images and then with both real and synthetic images (synthetic images in the train set only)
    
    ![](https://i.imgur.com/eelcC7w.png "Results Graph")

## Dataset

All our models and evaluations have utilised the Chest Xray14 dataset:
[ChestXray14](https://nihcc.app.box.com/v/ChestXray-NIHCC)

## Other credits

- PGGAN Implementation:
Segal, Bradley, et al. “Evaluating the Clinical Realism of Synthetic Chest x-Rays Generated Using Progressively Growing Gans.” SN Computer Science, vol. 2, no. 4, 2021, https://doi.org/10.1007/s42979-021-00720-7.
- Dreambooth:
https://colab.research.google.com/github/TheLastBen/fast-stable-diffusion/blob/main/fast-DreamBooth.ipynb
- Classification Model: 
https://www.kaggle.com/code/heyytanay/xray-image-eda-classification-keras/notebook
