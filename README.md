# DeepForest-Demos
A set of Jupyter Notebooks for trying out DeepForest Python library (keras-retinanet implementation). DeepForest is a python package for tree-crown detection from airborne RGB Imagery. The documentation for DeepForest (keras-retinanet implementation) can be found [here](https://deepforest.readthedocs.io/en/latest/)

## Contents
This repository contains trial notebooks for playing around with the DeepForest library and understand it's working.

- A Jupyter Notebook With Train/Predict using the `release_model` NEON.h5 (latest release `v.0.3.0`)
- A Jupyter Notebook with Train/Predict using a scratch model (keras-resnet50 backbone) trained on 40 images
containing around 700+ trees. 

### Training Hardware

- Processor : AMD Ryzen R5
- RAM : 8 GB DDR5
- GPU : Radeon RX 560X 

**Training Time :** ~ 8 - 12 mins/epoch

Note : Above GPU couldn't be used for training purpose as CUDA's interface model is meant for NVIDIA

### Results Obtained

- Train Using `release_model`
   - Image Tile Trained On : 40 Rasters (774 Trees)
   - Epochs : 5
   - mAP Obtained : 0.672

- Train Using `scratch_model`
   - Image Tile Trained On : 40 Rasters (774 Trees)
   - Epochs : 10
   - mAP Obtained : 0.274

### Conclusion
The `release_model` is trained on a huge dataset provided by National Ecological Observatory Framework, hence training data on top of this pre-built model is meant to give better mean average precision values. If, a model is to be trained using only the keras-resnet50 backend it would take a huge amount of data for `mAP > 0.5`.
