# Seq_nms_YOLO

#### Membres: Yunyun SUN, Yutong YAN, Sixiang XU, Heng ZHANG

---

## Introduction

![](img/index.jpg) 

This project combines **YOLOv2**([reference](https://arxiv.org/abs/1506.02640)) and **seq-nms**([reference](https://arxiv.org/abs/1602.08465)) to realise **real time video detection**.

## Installation
1. Create the repository without a readme and use the third option for cloning the repository. Insert `https://github.com/melodiepupu/seq_nms_yolo` for this step.
2. On your computer, choose a path and make a python 2 virtual enviroment `virtualenv -p python2 yolo_env`
3. Avtivate the enviroment using `source yolo_env/bin/activate' 
4. Install the requeriments using `conda install -y -c conda-forge opencv`, `conda install -y matplotlib Pillow scipy tensorflow`, `conda install -y -c conda-forge tf_object_detection`
5. Now clone the GitHub proyect by using `git clone https://github.com/hectordavideps/seq_nms_yolo.git`
6. Go to the repository using cd on terminal and now download weights running `wget https://pjreddie.com/media/files/yolo.weights` and `wget https://pjreddie.com/media/files/yolov2-tiny-voc.weights`first for yolo.weight, second for tiny.weights.
## Steps

1. `make` the project;
1. Download `yolo.weights` and `tiny-yolo.weights` by running `wget https://pjreddie.com/media/files/yolo.weights` and `wget https://pjreddie.com/media/files/tiny-yolo-voc.weights`;
1. Copy a video file to the video folder, for example, `input.mp4`;
1. In the video folder, run `python video2img.py -i input.mp4` and then `python get_pkllist.py`;
1. Return to root floder and run `python yolo_seqnms.py` to generate output images in `video/output`;
1. If you want to reconstruct a video from these output images, you can go to the video folder and run `python img2video.py -i output`

And you will see detection results in `video/output`

## Reference

This project copies lots of code from [darknet](https://github.com/pjreddie/darknet) , [Seq-NMS](https://github.com/lrghust/Seq-NMS) and  [models](https://github.com/tensorflow/models).
