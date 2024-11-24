# 通过多元辅助培训从图像中生成诗歌
论文中描述的 image-to-poem 模型的实现： “超越叙事描述：通过多对抗训练从图像中生成诗歌


### 介绍

模型是一个深度神经网络，可学习如何从图像生成诗歌

### 安装所需软件包
(建议在 Conda 环境下安装依赖项）
* python2.7  
* tensorflow1.6  
* mxnet  
* opencv  
* tqdm  
* colorama  
* flask

### 准备培训数据

| Name | #Poem | #Line/poem | #Word/line |
| :------:| :------: | :------: | :-----: |
| MultiM-Poem | 8,292 | 7.2 | 5.7 |
| UniM-Poem | 93,265 | 5.7 | 6.2 |
| MultiM-Poem(Ex) | 26,161 | 5.4 | 5.9 |

这两个数据集都以 JSON 文件格式呈现。

MultiM-Poem.json：图像和诗歌对

```json
[
    {
        "poem": str,
        "image_url": str,
        "id": int
    },
    ...
]
```

UniM-Poem.json：诗歌语料库

```json
[
    {
        "poem": str,
        "id": int
    },
    ...
]
```


### 下载训练模型
请从 https://1drv.ms/u/s!AkLgJBAHL_VFgSyyfpeGyGFZux56 下载模型，并将其放在 “code/”下。

## 创作诗歌
以下命令行将为图像生成诗歌。
```bash
python test.py
```
在控制台中键入测试图像的相对路径，然后就会生成诗歌
```bash
../images/test.jpg
```

输出示例
```txt
太阳在森林的风中歌唱
让我们迎着太阳之风而去
让太阳自由
让我们成为天堂的风暴
让我们成为缓慢的太阳
我们凝聚自己的力量
我们生活在爱与恨中
```

## 结果

以通过八种图像方法生成的诗歌的一些示例。



