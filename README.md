# Pneumo Vision

This is a computer vision machine learning model to classify chest xray images as having pneumomnia or not. 

> **Note:** this is not a novel problem or solution to the problem. I wrote this notebook as a means of exercising HuggingFace and PyTorch knowledge in the computer vision space, and I am by no means a xray imaging expert or am being paid to develop this code. Please use it with your own discretion.

## Model Architecture

The model uses a Vision Transformer (ViT) architecture; actually it uses the [google/vit-base-patch16-224-in21k](https://huggingface.co/google/vit-base-patch16-224-in21k) pre-trained open source model (Apache 2.0 license) which is a ViT model pre-trained on ImageNet-21k (14 million images, 21,843 classes) at 224x224 resolution. 

Next, the model is fine-tuned on a sample dataset [keremberke/chest-xray-classification](https://huggingface.co/datasets/keremberke/chest-xray-classification) which contains 4077 training, 582 test, and 1165 validation images.

## Running

To run yourself, I recommend using Poetry to setup a Python virtual environment with the necessary dependencies and then use the .ipynb notebook.

```shell
poetry install
poetry shell
```
