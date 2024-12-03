## Preparation

#### Environment

We test our codebase with PyTorch 1.12.1 with CUDA 11.6. Please install corresponding PyTorch and CUDA versions according to your computational resources. Then install the rest of required packages by running `pip install -r requirements.txt`. Please follow ```DATASET.md``` to download all the 11 datasets we used for experiments. We adapt this from [CoOp](https://github.com/KaiyangZhou/CoOp/blob/main/DATASETS.md).

#### Extracting Few-Shot Features

You can extract the features by running ``` CUDA_VISIBLE_DEVICES=0 python extract_features.py```.

## Usage

You can simply run ```CUDA_VISIBLE_DEVICES=0 python main.py --config configs/[dataset_name].yaml --shot [shot_number]``` to train and test the SimNL model. 

Here, `dataset_name` should be one of `[caltech101, dtd, eurosat, fgvc, food101, imagenet, oxford_flowers, oxford_pets, stanford_cars, sun397, ucf101]`, and `shot_number` is chosen from 1/2/4/8/16.
