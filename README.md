# Disentangled and Recurrent Prompt Tunning (DRPT)


## Setup
```
conda create --name clip python=3.7
conda activate clip
pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
pip3 install git+https://github.com/openai/CLIP.git
```
Alternatively, you can use `pip install -r requirements.txt` to install all the dependencies.

## Download Dataset
We experiment with three datasets: MIT-States, UT-Zappos, and C-GQA.
```
sh download_data.sh
```

If you already have setup the datasets, you can use symlink and ensure the following paths exist:
`data/<dataset>` where `<datasets> = {'mit-states', 'ut-zappos', 'cgqa', 'clevr'}`.


## Training
```
python -u train.py --dataset <dataset>
```

### Evaluation
```
python -u test.py --dataset <dataset>
```
You can replace `--dataset` with `{mit-states, ut-zappos, cgqa, clevr}`.


## References
If you use this code, please cite
```
@article{lu2022decomposed,
  title={Combating Data Imbalances in Federated Semi-supervised Learning with Dual Regulators},
  author={Sikai Bai, Shuaicheng Li, Weiming Zhuang, Kunlin Yang, Jun Hou, Shuai Yi, Shuai Zhang, Junyu Gao, Jie Zhang, Song Guo},
  journal={arXiv preprint arXiv:2307.05358},
  year={2023}
}
```
