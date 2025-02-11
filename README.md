# SSD-TS
Code for the paper: "SSD-TS: Exploring the potential of linear state space models for diffusion models in time series imputation"

## Requirements
Python==3.10.15

torch==2.3.1

cuda==11.8

mamba_ssm==2.2.2

causal_conv1d==1.4.0

## Experiments

First modify the config in `./config`

train for specific dataset:
```bash
python train.py --config path_to_your_config
```

inference for specific dataset:
```bash
python inference.py --config path_to_your_config
```
If you want to build your own imputer, modify `./imputers` according to the imputer files.


For mujoco dataset:
```bash
python train.py --config ./config/config_bissm2_mujoco_90_large.json
```
For ablation studies:

modify `line 16` in `train.py` and `line 9` in `inference.py` to corresponding imputers in `.\imputers\` 
