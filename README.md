# Detectron2
---

#### Whats Detectron2?

1. Open source **Object Detection and Segmentation Framework** developed by facebook AI research.
2. Built on top of Pytorch and provides a unified API for variety  of tasks, including, detection, instance segmentation, panoptic segmentation.
3. It includes high quality implementations of SOTA algorithms like Mask RCNN, RetinaNet, DensePose.
4. (Installing individual models from RCNN family like mask Rcnn is pain in the ass), hence, we can use Detectron2 for the same purpose.
5. It includes Model Zoo (collection of pre-trained models that are readily available for use)
   

#### How does Detectron2 work?
1. It uses a two-stage approach to object detection:
   - 1. It uses RPN to generate set of candidate regions.
     2. It uses mask RCNN model to classify and segment the candidate regions.

![image](https://github.com/user-attachments/assets/795030bc-7969-485e-be61-99fd7f6690ee)

#### What's panoptic segmentation ?
- Its combines semantic segmentation + instance segmentation to provide a comprehensive understanding of the scene.
- Use case - Autonomous Driving tasks
  
![image](https://github.com/user-attachments/assets/6773561f-29c5-4a9d-b1c7-bbd2a2e0ef7b)


#### Let's implement segment images using pre-trained models

```python
# Note: This is a faster way to install detectron2 in Colab, but it does not include all functionalities (e.g. compiled operators).
# See https://detectron2.readthedocs.io/tutorials/install.html for full installation instructions
!git clone 'https://github.com/facebookresearch/detectron2'
```

## Fine tuning Detectron2 for instance segmentation using custom data
---

Data Sets -
Data annotated for 4 classes:
1: Cell
2: Mitochondria​
3: Alpha granule​
4: Canalicular vessel​

Annotations were done using Makesense: https://www.makesense.ai/

Dataset from: https://leapmanlab.github.io/dense-cell/

coco-style json format annotations

![image](https://github.com/user-attachments/assets/2e8999a6-d2c1-432f-ad7e-2ea97200e148)




