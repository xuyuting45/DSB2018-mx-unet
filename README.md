用MXNet复现了U-net结构，参考了kaggle上data-science-bowl-2018比赛的toturial kernel，
https://github.com/kamalkraj/DATA-SCIENCE-BOWL-2018

主要的改进是：
1.数据预处理部分找出了每个细胞核的边缘，在训练时作为map的加权权重；
2.数据预处理部分用mask减去overlap，使得groundtruth上两个相邻的细胞核之间出现分隔带；
3.数据增强，使用了随机剪裁，镜像，颜色变换等技巧。

未完待续...
对检测结果进行后处理，用分水岭等数字图像处理技巧处理边缘。