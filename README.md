# Tensorflow Object Detection Final Project

This repository contains the final project for a Tensorflow Object Detection model. The project utilizes the Tensorflow Object Detection API to identify and classify objects within images.

## Project Overview

The project focuses on developing a semi-automated annotation pipeline for construction plans using TensorFlow's Object Detection API. The system annotates architecture drawings, labels key components, and estimates the sizes of objects within the images.

## Installation

To set up the project environment, you need to install certain packages and dependencies:

apt-get install protobuf-compiler python-pil python-lxml python-tk
pip install Cython

Then clone the TensorFlow models repository and set up the environment:

git clone https://github.com/tensorflow/models.git
cd models/research
protoc object_detection/protos/*.proto --python_out=.
set_env PYTHONPATH=$PYTHONPATH:pwd:pwd/slim


Finally, test the installation by running the model builder test script:

python object_detection/builders/model_builder_test.py


## Usage

The project includes scripts to process images through the trained object detection model. The main steps are as follows:

1. Annotate images using LabelImg.
2. Train a custom YOLOv8 object detection model on the annotated images.
3. Write scripts to convert model outputs to various formats such as YOLO, Pascal VOC.
4. Run the model on test images and visualize the results with bounding boxes and labels.

## Contribution

This project was completed as part of the Capstone Competition at Woosong University in 2023, where it won the first place award. The annotation process has achieved 85% automation, significantly reducing the manual workload.

Feel free to explore the notebooks and scripts, and contribute to the project by submitting pull requests or creating issues for any bugs or improvements you identify.

## License

[MIT License](LICENSE)


