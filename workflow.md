1. 克隆仓库

    ```bash
    git clone git@github.com:cucu9999/minimind.git
    # just4use
    git clone https://github.com/cucu9999/minimind.git
    ```

2. 下载模型

    ```bash

    ```

3. 环境配置

    ```bash
    conda create -n minimind python==3.10.16
    pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
    ```

4. 数据集准备

    ```bash
    https://www.modelscope.cn/datasets/gongjy/minimind_dataset/files
    ```
    > 1. 预训练阶段：pretrain_hq.jsonl   位于./dataset目录下 
    > 2. 微调阶段：sft_mini_512.jsonl   位于./dataset目录下


- 模型训练

位于/trainer目录下
```bash

python train_pretrain.py

torchrun --nproc_per_node 2 train_pretrain.py
```