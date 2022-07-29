#  Transformer Meets Convolution: A Bilateral Awareness Network for Semantic Segmentation of Very Fine Resolution Urban Scene Images

⭐ [Welcome to my HomePage](https://lironui.github.io/) ⭐ 

In this repository, we implement the Bilateral Awareness Network which contains a dependency path and a texture path to fully capture the long-range relationships and fine-grained details in very fine resolution (VFR) urban scene images . 

The detailed results can be seen in the [Transformer Meets Convolution: A Bilateral Awareness Network for Semantic Segmentation of Very Fine Resolution Urban Scene Images](https://www.mdpi.com/2072-4292/13/16/3065).

The training and testing code can refer to [GeoSeg](https://github.com/WangLibo1995/GeoSeg).

The related repositories include:
* [MACU-Net](https://github.com/lironui/MACU-Net)->A modified version of U-Net.
* [MAResU-Net](https://github.com/lironui/MAResU-Net)->A ResNet-based network with attention mechanism.
* [Multi-Attention-Network](https://github.com/lironui/Multi-Attention-Network)->A network with multi kernel attention mechanism.

If our code is helpful to you, please cite:

`Wang, L.; Li, R.; Wang, D.; Duan, C.; Wang, T.; Meng, X. Transformer Meets Convolution: A Bilateral Awareness Network for Semantic Segmentation of Very Fine Resolution Urban Scene Images. Remote Sensing. 2021, 13, 3065. https://doi.org/10.3390/rs13163065`

Requirements：
------- 
```
numpy >= 1.16.5
PyTorch >= 1.3.1
sklearn >= 0.20.4
tqdm >= 4.46.1
imageio >= 2.8.0
timm >= 0.4.5
```

Network:
------- 
![network](https://github.com/lironui/BANet/blob/main/figure/network.png)  
Fig. 1.  The overall architecture of BANet.

Result:
------- 
The result on the [UAVid dataset](https://uavid.nl/) can seen from [here, where the user name is **AlexWang**](https://competitions.codalab.org/competitions/25224#results) and the results can be downloaded by this [**link**](https://competitions.codalab.org/my/competition/submission/903899/input.zip):

| Method    | building | tree     | clutter   | road     | vegetation | static car | moving car | human    | mIoU     | 
|-----------|----------|----------|-----------|----------|------------|------------|------------|----------|----------| 
| MSD       | 79.8     | 74.5     | 57.0      | 74.0     | 55.9       | 32.1       | 62.9       | 19.7     | 57.0     | 
| Fast-SCNN | 75.7     | 71.5     | 44.2      | 61.6     | 43.4       | 19.5       | 51.6       | 0.0      | 45.9     | 
| BiSeNet   | **85.7** | 78.3     | 64.7      | 61.1     | **77.3**   | **63.4**   | 48.6       | 17.5     | 61.5     | 
| SwiftNet  | 85.3     | 78.2     | 64.1      | 61.5     | 76.4       | 62.1       | 51.1       | 15.7     | 61.1     | 
| ShelfNet  | 76.9     | 73.2     | 44.1      | 61.4     | 43.4       | 21.0       | 52.6       | 3.6      | 47.0     | 
| BANet     | 85.4     | **78.9** | **66.6**  | **80.7** | 62.1       | 52.8       | **69.3**   | **21.0** | **64.6** | 


![Result](https://github.com/lironui/BANet/blob/main/figure/UAVid%20-%20val.png)  
Fig. 2. The experimental results on the UAVid validation set. The first column illustrates the input RGB images, the second column depicts the ground reference and the third column shows the predictions of our BANet.

![Result](https://github.com/lironui/BANet/blob/main/figure/UAVid.png)  
Fig. 3.  The experimental results on the UAVid test set. The first column illustrates the input RGB images, the second column depicts the outputs of MSD and the third column shows the predictions of our BANet. 

