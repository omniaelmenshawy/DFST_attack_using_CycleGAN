
# Deep Feature Space Trojan (DFST) Attack Implementation and Evaluation

This repository contains an implementation of the DFST attack, as proposed in a scientific paper called Deep Feature Space Trojan Attack of Neural Networks by Controlled Detoxification: https://arxiv.org/abs/2012.11212.
 The aim of this project is to understand adversarial attacks and defenses in machine learning, demonstrating the potential vulnerability of machine learning models to such attacks.

## The project is split into three main parts:

- Training two deep learning models on the CIFAR-10 dataset.
- Implementing the DFST attack.
- Implementing a detoxification process to neutralize the trojan attack.

In the end, the performance of the models is evaluated before and after the attack and detoxification to provide an assessment of the attack's success and the detoxification's effectiveness.

## Getting Started

This project is built using Python and relies on PyTorch for the implementation of the deep learning models and the adversarial attacks.

Before running the code, ensure that you have the correct environment with all the necessary dependencies installed. The code will run on a GPU if available; otherwise, it will default to a CPU.

## Project Structure

The project is organized into three primary sections:

- model_training: This directory contains the Python scripts for training the two deep learning models, a custom Convolutional Neural Network (CNN) and a pre-trained ResNet50 model, on the CIFAR-10 dataset.
- dfst_attack: This directory holds the Python scripts for implementing the DFST attack. The process starts with generating a trigger image using a CycleGAN, applying this trigger to a subset of the training dataset to create poisoned data, and then retraining the models with this poisoned dataset.
- detoxification_process: In this directory, you will find the Python scripts for implementing the detoxification process. This involves identifying the compromised neurons, training a Feature Injector to correct their outputs, and integrating this Feature Injector into the poisoned models.

## Evaluation

The performance of the models is evaluated before and after the attack and detoxification using a test dataset. Both batch and single image evaluations are performed. The evaluation results are printed to the console and also visualized.

Batch evaluation provides the overall accuracies of the models under normal and attack scenarios. Confusion matrices are also plotted to provide a visual representation of the models' performances.

Single image evaluation provides a more detailed analysis for individual images, and includes plotting of the original image, the trigger image, and the attacked image side by side.

## Results: 

<img width="877" alt="Screen Shot 2023-05-31 at 22 52 59" src="https://github.com/omniaelmenshawy/DFST_attack_using_CycleGAN/assets/77496383/502517f9-5255-497a-b73c-b95b105d20ee">

<img width="952" alt="Screen Shot 2023-05-31 at 22 53 23" src="https://github.com/omniaelmenshawy/DFST_attack_using_CycleGAN/assets/77496383/efd6eb76-8a30-4876-8148-1995a53d60c7">

<img width="938" alt="Screen Shot 2023-05-31 at 22 54 02" src="https://github.com/omniaelmenshawy/DFST_attack_using_CycleGAN/assets/77496383/dda39439-85fc-4604-9200-a2e3f3b7951a">

<img width="618" alt="Screen Shot 2023-05-31 at 22 54 25" src="https://github.com/omniaelmenshawy/DFST_attack_using_CycleGAN/assets/77496383/c7accdba-ccb3-4a72-a4fd-791d801c7d73">
<img width="701" alt="Screen Shot 2023-05-31 at 22 54 51" src="https://github.com/omniaelmenshawy/DFST_attack_using_CycleGAN/assets/77496383/6a7e770b-dde2-4701-acb4-a59aa623dfb2">

## Acknowledgments

This project is part of a term project for the Adversarial Machine Learning course implemented with my colleage Qatrelnada Almarzoq and under the supervision of Prof. Ehsan Nowrozi in the department of Artificial Intelligence Engineering in Bahcesehir University. It serves as a hands-on exploration of the implementation of adversarial attacks in machine learning, fostering a deeper understanding of the field. It also validates the results of the original paper on the DFST attack, contributing to transparency and reliability in machine learning research.

## Disclaimer

This code is for educational purposes only. The paths and images used in the code are placeholders and would need to be replaced with appropriate paths and images for real-world implementation.
