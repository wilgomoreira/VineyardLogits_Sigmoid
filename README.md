# dataset_vineyardLogits_sigmoid

## Overview
The **dataset_vineyardLogits_sigmoid** dataset is a collection of logits and labels used for training and testing deep learning models in the field of precision agriculture. **All models were trained for a binary classification task, using a single class and the sigmoid activation function** to output probabilities. This ensures that the models are optimized for distinguishing between vine plants and background elements in the images.

## Hyperparameters 

In this project, we work with **three distinct datasets** for a **binary classification task**. Below is a summary of the key hyperparameters used during training and testing:

1. **Split ratio**:  
   Each dataset is split into training and testing sets with a ratio of **80:20**. This means that 80% of the data is used for training the model, while 20% is reserved for testing and evaluating its performance.

2. **Learning Rate**:  
   The initial learning rate is set to **0.001**. The learning rate controls how much to change the model in response to the estimated error each time the model weights are updated.

3. **Batch Sizes**:  
   The **BATCH_SIZE_TRAIN** is **30**, meaning that during training, the model processes 30 samples before updating the model's parameters. For testing, we use a smaller **BATCH_SIZE_TEST** of **3** samples at a time, ensuring efficient evaluation of model performance on smaller portions of the data.

These hyperparameters were chosen to strike a balance between training stability and performance, and they are tailored to handle the size and complexity of the datasets used in this project.

## Dataset Structure

```plaintext
dataset_vineyardLogits_sigmoid
├── deeplab_EARLY_FUSION_fold_1
├── deeplab_EARLY_FUSION_fold_2
├── deeplab_EARLY_FUSION_fold_3
├── deeplab_GNDVI_fold_1
├── deeplab_GNDVI_fold_2
├── deeplab_GNDVI_fold_3
├── deeplab_NDVI_fold_1
├── deeplab_NDVI_fold_2
├── deeplab_NDVI_fold_3
├── deeplab_RGB_fold_1
├── deeplab_RGB_fold_2
├── deeplab_RGB_fold_3
├── segnet_EARLY_FUSION_fold_1
├── segnet_EARLY_FUSION_fold_2
├── segnet_EARLY_FUSION_fold_3
├── segnet_GNDVI_fold_1
├── segnet_GNDVI_fold_2
├── segnet_GNDVI_fold_3
├── segnet_NDVI_fold_1
├── segnet_NDVI_fold_2
├── segnet_NDVI_fold_3
├── segnet_RGB_fold_1
├── segnet_RGB_fold_2
├── segnet_RGB_fold_3
└── README.md
```

## Contents

- **model_modality_fold_n/pred_masks_train**: This directory contains the model logits in train
- **model_modality_fold_n/pred_masks_test**: This directory contains the model logits in test
  
## Data Description

- **Model logits**: The data used in this study consists of logits obtained from the deep model (SegNet and DeepLabV3) during training and testing mode. These logits represent the unnormalized predictions (raw scores) before applying any activation function, in this case, **sigmoid**.
- **Original images**: The images originate from aerial multispectral imagery collected from three vineyards in central Portugal: Quinta de Baixo (QTA), ESAC, and Valdoeiro (VAL). Captured at a resolution of 240x240 pixels, these images were obtained using an unmanned aerial vehicle (UAV) equipped with an X7 RGB camera and a MicaSense Altum multispectral sensor. The dataset comprises RGB and near-infrared (NIR) bands, facilitating the calculation of vegetation indices such as NDVI and GNDVI. Ground-truth annotations for vine plants are included, enabling a thorough evaluation of the models. For more details, please refer to the dataset titled "DL Vineyard Segmentation Study," available at the following link: [Cybonic, "DL Vineyard Segmentation Study," v1.0, GitHub, 2024](https://github.com/Cybonic/DL_vineyard_segmentation_study).

## Usage

To use the weights in your model, follow these steps:

```bash
git clone https://github.com/wilgomoreira/dataset_vineyardLogits_sigmoid.git
```

## License

This dataset is licensed under the MIT License. Please ensure to comply with the license terms when using this dataset.

## Acknowledgments

**Wilgo Cardoso** for creating the dataset.

## Contact

For questions or further information, please contact:
[wilgo.moreira@isr.uc.pt](mailto:wilgo.moreira@isr.uc.pt)

