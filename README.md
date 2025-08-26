# HVCL

<img width="2232" height="663" alt="image" src="https://github.com/user-attachments/assets/d32d6dc0-9ed0-476f-832c-4c3711dae2d8" />



## Installation and Requirements

Please note that our environment requirements are different from LLaVA's environment requirements. We strongly recommend you create the environment from scratch as follows.

1. Clone this repository and navigate to the folder
```bash
git clone https://github.com/HVCL/HVCL.git
cd HVCL
```

2. Create a conda environment, activate it and install Packages
```Shell
conda create -n hvcl python=3.10 -y
conda activate hvcl
pip install --upgrade pip  # enable PEP 660 support
pip install -e .
```

3. Install additional packages
```Shell
pip install flash-attn --no-build-isolation
```
#### Upgrade to the latest code base

```Shell
git pull
pip install -e .
```

## Get Started

#### 1. Data Preparation

Please refer to the [Data Preparation](https://tinyllava-factory.readthedocs.io/en/latest/Prepare%20Datasets.html) section in our [Documenation](https://tinyllava-factory.readthedocs.io/en/latest/).

#### 2. Train

Here's an example for training a LMM using Phi-2.

- Replace data paths with yours in `scripts/train/train_phi.sh`
- Replace `output_dir` with yours in `scripts/train/pretrain.sh`
- Replace `pretrained_model_path` and `output_dir` with yours in `scripts/train/finetune.sh`
- Adjust your GPU ids (localhost) and `per_device_train_batch_size` in `scripts/train/pretrain.sh` and `scripts/train/finetune.sh`

```bash
bash scripts/train/train_phi.sh
```


#### 3. Evaluation

Please refer to the [Evaluation](https://tinyllava-factory.readthedocs.io/en/latest/Evaluation.html) section in our [Documenation](https://tinyllava-factory.readthedocs.io/en/latest/Evaluation.html).



#### Model Performance

| VT (HF Path)                      | LLM (HF Path)                       | VQA-v2 | GQA  | SQA-image | TextVQA | MM-Vet | POPE | MME    | MMMU-val |
| --------------------------------- | ----------------------------------  | :----: | :--: | :-------: | :-----: | :----: | :--: | :----: | :------: |
| google/siglip-so400m-patch14-384  | microsoft/phi-2                     | 80.96   | 64.14 | 71.59     | 59.23   |36.1  | 88.67 | 1488.96 | 37.3    |

### Legacy Models

Comparison of experimental results.
<img width="1300" height="993" alt="image" src="https://github.com/user-attachments/assets/0acbb6d3-dade-44db-a3d8-0b998ae2934d" />






## Contact
If you have any questions, feel free to either initiate an *Issue* .




## ❤️ Community efforts
* Our codebase is built upon the [TinyLLaVA]([https://github.com/haotian-liu/LLaVA](https://github.com/TinyLLaVA/TinyLLaVA_Factory)) project. Great work!
