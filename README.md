# R2Gen-Mamba

This is the implementation of [R2Gen-Mamba: A Selective State Space Model for Radiology Report Generation]





## Requirements

- `torch==1.12.1`
- `torchvision==0.8.2`
- `opencv-python==4.4.0.42`


## R2Gen-Mamba Models

The pre-trained R2Gen-Mamba models on different datasets. You can download the models and run them on the corresponding datasets to replicate our results.

| Section   | BaiduNetDisk                                                 | GoogleDrive                                                  | Description                               |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ |-------------------------------------------|
| IU X-Ray  | [download](https://pan.baidu.com/s/1I7LFRXKO59xs5jX2ZI6Vlg?pwd=9e8m) (Password: 9e8m) | [download](https://drive.google.com/file/d/1HWmgl64SDjc6ABpZOQPj3xZKN4T5s_Mo/view?usp=sharing) | R2Gen-Mamba model trained on **IU X-Ray** |
| MIMIC-CXR | [download](https://pan.baidu.com/s/1grCHBnMZa64R9WoRsJeiPw?pwd=auii) (Password: auii) | [download](https://drive.google.com/file/d/1qtgHTn99xIIbsP7DYzwa3kvOqoU8ewUJ/view?usp=sharing) | R2Gen-Mamba model trained on **MIMIC-CXR**      |



## Datasets
We use two datasets ([IU X-Ray][iu-xray_link] and [MIMIC-CXR][MIMIC-CXR_link]) in our paper.

[iu-xray_link]:http://openi.nlm.nih.gov/
[MIMIC-CXR_link]:https://physionet.org/content/mimic-cxr-jpg/2.1.0/

## Train

Run `bash train_iu_xray.sh` to train a model on the IU X-Ray data.

Run `bash train_mimic_cxr.sh` to train a model on the MIMIC-CXR data.

## Test

Run `bash test_iu_xray.sh` to test a model on the IU X-Ray data.

Run `bash test_mimic_cxr.sh` to test a model on the MIMIC-CXR data.

Follow or [CheXbert](https://github.com/stanfordmlgroup/CheXbert) to extract the labels and then run `python compute_ce.py`. Note that there are several steps that might accumulate the errors for the computation, e.g., the labelling error and the label conversion. We refer the readers to those new metrics, e.g., [RadGraph](https://github.com/jbdel/rrg_emnlp) and [RadCliQ](https://github.com/rajpurkarlab/CXR-Report-Metric).

## Visualization

Run `python help.py` to visualize the attention maps on the MIMIC-CXR data.

## Acknowledgements
This project is developed based on [R2Gen](https://github.com/zhjohnchan/R2Gen), and we appreciate their original work and open-source contribution.
