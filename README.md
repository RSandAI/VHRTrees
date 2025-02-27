# VHRTrees

This repository contains weights for YOLOv5, YOLOv7, YOLOv8, and YOLOv9 networks trained with the VHRTrees dataset. 

# Dataset Details
The imagery required for the dataset has been obtained from Google Earth. We have downloaded 218 RGB images, each with a resolution of 1920x1080 pixels and a ground sample distance (GSD) of 0.5 km, covering the districts of Karacabey in Bursa, Turkey and Dikili, Aliağa, Seferihisar, and Selçuk in İzmir, Turkey. A sample image and corresponding minimum boxes for trees can be seen the figure. The dataset has been approximately split as 70% (1023 images), 15% (226 images) and 15% (222 images) for training, validation and testing, respectively.

![sample_2_github1](https://github.com/RSandAI/VHRTrees/blob/main/Dataset_details.jpg)

# Models, Metric Results and Weights

Experiments were conducted on Kaggle P100, Colab A100, and NVIDIA Quadro P6000 GPUs. All experiments were conducted on powerful GPUs and executed concurrently, resulting in similar durations. The evaluation results of the top-performing eight experiments are presented in the table below.


| Experiment No | Network | Optimizer |     Model     | Batch Size | Epoch | F-1 Score | Precision | Recall | mAP50 | mAP50-95 | Link |
|:-------------:|:-------:|:---------:|:-------------:|:----------:|:-----:|:---------:|:---------:|:------:|:-----:|:--------:|--------  |
|     Exp-1     | 960x960 |    Auto   |    YOLOv8m    |     16     |   50  |   0.932   |   0.932   |  0.932 | 0.934 |   0.608  | [Download](https://drive.google.com/file/d/1DO785NH13fEleCrQeLQb9L7SSyb1tEiT/view?usp=drive_link) |
|     Exp-2     | 960x960 |    SGD    |    YOLOv8m    |     16     |   50  |   0.915   |   0.942   |  0.890 | 0.916 |   0.608  | [Download](https://drive.google.com/file/d/1pviwFw14uib14890b1HzZ6qr-yRlt8UW/view?usp=drive_link) |
|     Exp-3     | 640x640 |    SGD    | YOLOv9-gelan-c|      8     |   45  |   0.928   |   0.924   |  0.932 | 0.936 |   0.594  | [Download](https://drive.google.com/file/d/1MqOBOPCP1jvX-LKQ05uQtcdyK7x2tF-I/view?usp=drive_link) |
|     Exp-4     | 640x640 |    SGD    | YOLOv9-gelan-c|      8     |   45  |   0.924   |   0.922   |  0.927 | 0.534 |   0.584  | [Download](https://drive.google.com/file/d/1KBYk0A8xtqcvdjkD4kDIJHudefanVZG1/view?usp=drive_link) |
|     Exp-5     | 960x960 |    SGD    |    YOLOv5m    |     16     |   50  |   0.929   |   0.932   |  0.926 | 0.934 |   0.569  | [Download](https://drive.google.com/file/d/1_fzjVl8yOYphNK2pyaJYR250Ckz0P46i/view?usp=drive_link) |
|     Exp-6     | 960x960 |    SGD    |    YOLOv5s    |     16     |   50  |   0.931   |   0.930   |  0.933 | 0.933 |   0.567  | [Download](https://drive.google.com/file/d/1ue-vPl4krs96CTbyxSca27FYdxQ8bziD/view?usp=drive_link) |
|     Exp-7     | 960x960 |    SGD    |   YOLOv7-X    |     16     |   50  |   0.930   |   0.923   |  0.937 | 0.912 |   0.552  | [Download](https://drive.google.com/file/d/17A36XziU33TWUOKy4ubspCPYhka3bV7-/view?usp=drive_link) |
|     Exp-8     | 960x960 |    SGD    |    YOLOv7     |     16     |   50  |   0.929   |   0.930   |  0.928 | 0.908 |   0.549  | [Download](https://drive.google.com/file/d/18KWTWqiuOx4iMVdYarsWR4Bx7SKFYbtF/view?usp=drive_link) |



# Visual Results

![figure3_visual_results](https://github.com/RSandAI/VHRTrees/blob/main/Visual_results_figure3.jpg)

# Citation:
Please kindly cite our [paper](https://www.frontiersin.org/journals/forests-and-global-change/articles/10.3389/ffgc.2024.1495544/full) if this code and the dataset used in the study are useful for your research.

Topgül, Ş. N., Sertel, E., Aksoy, S., Ünsalan, C., & Fransson, J. E. S. (2024). VHRTrees: A New Benchmark Dataset for Tree Detection in Satellite Imagery and Performance Evaluation with YOLO-based Models. Frontiers in Forests and Global Change, 7. doi.org/10.3389/ffgc.2024.1495544.
