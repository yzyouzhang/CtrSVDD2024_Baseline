# SVDD Challenge Baseline Systems
This repository contains the baseline system implementations for the SVDD Challenge 2024. To form a comprehensive evaluation, we implemented the front-end features, back-end systems and the evaluation metrics. The baseline systems are implemented in Python and are available as open-source software.

# Getting Started

Setting up environment:
```bash
conda create -n svdd_baseline python=3.10
conda activate svdd_baseline
pip install -r requirements.txt
```

Then you can run the training script with the following command:
```bash
python train.py --base_dir {Where the data is} --gpu {GPU ID} --encoder {Encoder Type} --batch_size {Batch size}
```

After training, you can evaluate your model using the following command:
```bash
python eval.py --base_dir {Where the data is} --model_path {The model's weights file} --gpu {GPU ID} --encoder {Encoder Type} --batch_size {Batch size}
```

The main functions in `train` and `eval` specify more options that you can tune. 

Within `base_dir`, the code expects to see `train_set`, `dev_set` and `test_set` directories, along with `train.txt` and `dev.txt` as open-sourced. `train_set`, `dev_set` and `test_set` should directly contain `*.flac` files.