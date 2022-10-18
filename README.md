# Guided Anchoring Cascade RCNN

> [Guided Anchoring Cascade R-CNN: An intensive improvement of R-CNN in Vietnamese Document Detection](https://ieeexplore.ieee.org/abstract/document/9701510)

<!-- [ALGORITHM] -->

## Abstract

Along with the development of the world, digital documents are gradually replacing paper documents. Therefore, the need to extract information from digital documents is increasing and becoming one of the main interests in the field of computer vision, particularly reading comprehension of image documents. The problem of object detection on image documents (figures, tables, formulas) is one of the premise problems for analyzing and extracting information from documents. Previous studies have mostly focused on English documents. In this study, we now experiment on a Vietnamese image document dataset UIT-DODV, which includes four classes: Table, Figure, Caption and Formula. We test on common state-of-the-art object detection models such as Double-Head R-CNN, Libra R-CNN, Guided Anchoring and achieved the highest results with Guided Anchoring of 73.6% mAP. Besides, we assume that high-quality anchor boxes are keys to the success of an anchor-based object detection models, thus we decide to adopt Guided Anchoring in our research. Moreover, we attempt to raise the quality of the predicted bounding boxes by utilizing Cascade R-CNN architecture, which can afford this by its scheme, so that we can filter out as many confused bounding boxes as possible. Based on the initial evaluation results from the common state-of-the-art object detection models, we proposed an object detection model for Vietnamese image documents based on Cascade R-CNN and Guided Anchoring. Our proposed model has achieved up to 76.6% mAP, 2.1% higher than the baseline model on the UIT-DODV dataset.

<div align=center>
<img src="https://i.imgur.com/jxLm4Vq.jpg"/>
</div>



## Results and models of Guided Anchoring Cascade RCNN on UIT-DODV dataset

|       Method       | Table  |  Figure  | Caption |  Formula | AP@.5 | AP@.75 | mAP |                                                                                 Config                                                                                  |                                                                                                                                                              Download                                                                                                                                                              |
| :----------------: | :-------: | :-----: | :-----: | :----------: | :-------: | :----: | :-----: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|     Double-Head R-CNN    | 91.5 | 80.6 | 65.6 | 46.3 | 88.7 | 78.4 | 71.0 |             [config](https://github.com/truong11062002/GA-CascadeRCNN/blob/main/dh_faster_rcnn_r50.py)              |                           [log]()                          |
|     Libra R-CNN    | 92.5 | 81.0 | 68.2 | 46.0 | 89.6 | 79.1 | 71.9 |       [config](https://github.com/truong11062002/GA-CascadeRCNN/blob/main/libra_faster_rcnn_x101.py)        |               [log]()              |
|     Guided Anchoring Faster R-CNN     | 92.7 | 81.6 | 73.3 | 46.9 | 91.0 | 80.8 | 73.6   |                   [config](https://github.com/truong11062002/GA-CascadeRCNN/blob/main/ga_faster_rcnn_x101.py)                   |                          [log]()                         |
|     CascadeTabNet + Fused Loss     | 94.3 | 83.0 | 73.3 | 47.5 | 89.1 | 81.6 | 74.5    |       [config]()       |             [log]()             |
|     Guided Anchoring Cascade R-CNN (Ours)     | 95.4 | 84.8 | 75.9 | 50.5 | 91.8 | 83.1 | 76.6 |           [config](https://github.com/truong11062002/GA-CascadeRCNN/blob/main/ga_cascade_rcnn_x101.py)            |                       [log]()

## Installation
- Please setup [UIT-DODV dataset](https://github.com/nguyenvd-uit/uit-together-dataset/blob/main/UIT-DODV.md) for MMDetection.

- This repository builds upon [MMDetection](https://github.com/open-mmlab/mmdetection). 
See [The MMDetection documentation](https://github.com/open-mmlab/mmdetection/blob/master/docs/en/get_started.md) for installation instructions.

## Citation

We provide config files to reproduce the document object detection performance in the NICS 2021 paper for [Guided Anchoring Cascade R-CNN: An intensive improvement of R-CNN in Vietnamese Document Detection](https://ieeexplore.ieee.org/abstract/document/9701510).

```latex
@inproceedings{le2021guided,
  title={Guided Anchoring Cascade R-CNN: An intensive improvement of R-CNN in Vietnamese Document Detection},
  author={Le, Hai and Nguyen, Truong and Le, Vy and Nguyen, Thuan Trong and Vo, Nguyen D and Nguyen, Khang},
  booktitle={2021 8th NAFOSTED Conference on Information and Computer Science (NICS)},
  pages={188--193},
  year={2021},
  organization={IEEE}
}
```
