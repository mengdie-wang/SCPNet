# SCPNet
SCPNet: Self-constrained Parallelism Network for Keypoint-based Lightweight Object Detection.  
Xian Zhong, Mengdie Wang, Wenxuan Liu, Jingling Yuan, Wenxin Huang.
## Highlight
- SCPNet can speed inference,drop parameters, and obtain more accurate boundary boxes.
- PMFM for feature extraction can maintain high-resolution and widen receptive field.
- SCDM proposes the distance constraint between geometric centers and center keypoints.

## Requirements
- Python 3
- TensorFlow 1.16
- OpenCV
- tqdm
- glob
- sys
- mmdet 2.6
- mmcv 1.1.5

## Dataset
```
|--MS-COCO 2017
        |annotations
                |instances_train2017.json
                |instances_test2017.json
                |instances_val2017.json  
        |--train2017
        |--test2017  
        |--val2017
```

## Training
Run the following commands:
```
python  mmdetection/tools/train.py config/centripetalnet_SCPNet.py
```

## Testing
Run the following commands:
```
python  mmdetection/tools/test.py config/centripetalnet_SCPNet.py
```
