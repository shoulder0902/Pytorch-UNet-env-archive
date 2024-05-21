所有命令需要在本项目根目录下使用

1. 安装环境
```shell
conda env create -f environment.yml
```

2. 切换环境
```shell
conda activate pytorch_unet
```

3. 根据224模型训练(已包含模型，可跳过)
```shell
python train.py -c 3
```

4. 根据224模型预测并查看预览(-v进行可视化，-n不保存图像)

* 自行训练后使用checkpoint：
```shell
python predict.py -i 需要预测的图像路径 -c 3 -m checkpoints/checkpoint_epoch5.pth -v -n
```

* 或者使用预训练的模型：
```shell
python predict.py -i 需要预测的图像路径 -c 3 -m MODEL.pth -v -n
```