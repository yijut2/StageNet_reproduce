## Introduction
The paper "StageNet: Stage-Aware Neural Networks for Health Risk Prediction" proposes a novel stage-aware neural network model (StageNet) for extracting disease stage information from patient data and integrating it into risk prediction. This repository is used to record the progress of paper reproducibility and all the revised models used. (We also created the descriptive notebook for bonus)

## Data Download Instruction
We do not provide the MIMIC-III data itself. You must acquire the data yourself from https://mimic.physionet.org/. Specifically, download the CSVs. To run decompensation prediction task on MIMIC-III bechmark dataset, you should first build benchmark dataset according to https://github.com/YerevaNN/mimic3-benchmarks/. (The instruction came from https://github.com/v1xerunt/StageNet)

## Citation
Junyi Gao, Cao Xiao, Yasha Wang, Wen Tang, Lucas M
Glass, and Jimeng Sun. 2020. Stagenet: Stageaware neural networks for health risk prediction. In Proceedings of The Web Conference 2020

## Dependency
Install python, pytorch. We use Python 3.7.3, Pytorch 1.1.
If you plan to use GPU computation, install CUDA

## Preprocessing code + command (if applicable)
Same as above, to acquire the MIMIC-III data, you can follow the steps provided in https://github.com/YerevaNN/mimic3-benchmarks/.

## Training code + command (if applicable)
The original command `$python train.py --data_path='./data/' --file_name='trained_model'` allows us to train the StageNet with default setting. It also allows users to specify hyperparameter. To observe our training process and analyze our training, we made the continueTrain argument equal to True, and train the model with different batchsize and epochs: `python ./drive/MyDrive/StageNet/train.py --data_path='./data/' --file_name='trained_model' --batch_size=64 --epochs 50 --continueTrain True`

## Pretrained model/weights (if applicable)
Run the `python ./drive/MyDrive/StageNet/train.py --data_path='./data/' --file_name='trained_model' --batch_size=64 --epochs 50 --continueTrain True`, and the script will automatically generated the best weights and it will be saved as the new file.

## Table of results
See the descriptive notebook, we providded the table of results with brief summary.
