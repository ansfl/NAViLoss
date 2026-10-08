&nbsp; &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp;  <img src="https://github.com/ansfl/MEMS-IMU-Denoising/blob/de1832c6fc4e07936bd36e13a5fab6fe5dfc78d3/figrues/Logo.png" />



# NAViLoss: An Underwater Navigation-Aware Dual-Residual Objective for Physics-Consistent Learning

[![arXiv](https://img.shields.io/badge/arXiv-2610.09690-b31b1b.svg)](https://arxiv.org/abs/2610.09690)

NAViLoss is a robust, uncertainty-aware objective for learning-based
velocity estimation in autonomous underwater vehicles (AUVs).

The proposed objective jointly considers velocity-estimation error and
DVL beam-consistency error while accounting for measurement uncertainty.

NAViLoss is integrated with DeepONet to develop NAVi-DeepONet models for
robust AUV velocity estimation under noisy measurements and partial DVL
beam-outage conditions.


## Framework Overview

<p align="center">
  <img src="figures/Navi-Deeponet.png" width="900">
</p>

<p align="center">
  <em>Overview of the proposed NAViLoss framework.</em>
</p>


## Key Contributions

1. A navigation-aware dual-residual objective for physics-consistent
   velocity estimation.

2. An uncertainty-aware robust loss that reduces the influence of
   large residuals.

3. NAVi-DeepONet models for full and partial DVL beam conditions.

4. Improved velocity-estimation performance under noisy and degraded
   DVL measurements.


## NAVi-DeepONet

<p align="center">
  <img src="figures/Navi-Deeponet.png" width="900">
</p>


<p align="center">
  <em>NAVi-DeepONet architecture.</em>
</p>


## Experimental Platform

<p align="center">
  <img src="https://raw.githubusercontent.com/ansfl/DVL-DeepONet/main/figures/snapir_auv.png" width="700">
</p>

<p align="center">
  <em>Snapir Autonomous Underwater Vehicle (AUV) used for data collection during Mediterranean Sea trials.</em>
</p>


## Results

### NAVi-DeepONet V1

| Model | VRMSE (m/s) | VMAE (m/s) | R² |
|-----------|------------:|------------:|----:|
| LS | 0.178 | 0.161 | 0.507 |
| BeamsNet | 0.116 | 0.104 | 0.706 |
| DVL-DeepONet | 0.092 | 0.074 | 0.869 |
| **NAVi-DeepONet V1** | **0.082** | **0.071** | **0.878** |


### NAVi-DeepONet V2

| Model | VRMSE (m/s) | VMAE (m/s) | R² |
|-----------|------------:|------------:|----:|
| ELC | 1.991 | 1.696 | -1.340 |
| MissBeamNet | 0.329 | 0.288 | -0.403 |
| DVL-DeepONet | 0.254 | 0.224 | 0.312 |
| **NAVi-DeepONet V2** | **0.175** | **0.142** | **0.694** |


## Files

- `main_NAViLoss.ipynb`
  - Demonstration of the proposed NAViLoss objective.

- `main_NAVi-DeepONet_V1.ipynb`
  - NAVi-DeepONet V1 for full DVL beam measurements.

- `main_NAVi-DeepONet_V2.ipynb`
  - NAVi-DeepONet V2 for partial DVL beam measurements.


## Usage

Open any notebook in Jupyter Notebook, JupyterLab, or Google Colab
and run the cells in order.


## Author

Arup Kumar Sahoo and Itzik Klein


## Citation

If you use this repository in your research, please cite:

```bibtex
@article{sahoo2026naviloss,
  title={NAViLoss: An Underwater Navigation-Aware Dual-Residual Objective
  for Physics-Consistent Learning},
  author={Sahoo, Arup Kumar and Klein, Itzik},
  journal={arXiv preprint arXiv:2610.09690},
  year={2026}
}
