# Ai-Algorithm
 # 代码说明

本项目包为AI算法组的主要算法实现：ResNet 、 YOLO等。以下是每个文件夹下的目录结构的详细说明：

## Algorithm

### resnet

此文件夹包含 ResNet 算法的实现。具体内容如下：

- **README_RESNET.md**：包含 ResNet 算法的说明和实现细节(TODO)。

### yolo

此文件夹包含 YOLO 算法的实现。具体内容如下：

- **README_YOLO.md**：YOLO算法总体README。
- **v5**：包含 YOLOv5 算法的实现。具体内容如下：
  - **v5_Custom**：包含自定义的 YOLOv5 算法实现(TODO)。
  - **v5_Original**：包含原始的 YOLOv5 算法实现（源码禁止改动，并附上版本及原始github带分支及tag的链接）。
- **v8**：包含 YOLOv8 算法的实现。具体内容如下：
  - **v8-Custom**：包含自定义的 YOLOv8 算法实现。
    - **custom_codes**：包含自定义的 YOLOv8 训练or检测or验证代码。
    - **train_cfgs**：包含自定义的训练配置文件。
    - **v8_scripts**：包含自定义的工具脚本。
  - **v8-Original**：包含原始的 YOLOv8 算法实现（源码禁止改动，并附上版本及原始github带分支及tag的链接）。
    - **ultralytics**：

## Datastes 
此文件夹下包含数据集等相关内容，待完善。

## Models
按模型结构及种类存放，注意按照命名规范（https://docs.qq.com/doc/DSUlXbWhua1BydElG）。

模型命名规范须遵循以下几项规范：

### 1. 第一项：按照模型用途命名

按照模型具体可实现的算法任务，结合具体使用场景，给模型进行简洁明了的命名，突出主体效用，例：

- 人体检测模型：PersonOD_（PersonObjectDetection）
- 人体关键点检测模型：PersonKpD_（PersonKeypointsDetection）
- 人脸关键点检测模型：FaceKpD_（FaceKeypointsDetection）
- 人体属性识别模型：PersonAttrsR_（PreosonAttributesRec）
- 人脸特征提取模型：FaceFeasE_（FaceFeaturesExtract）

分类模型只需要根据主体任务或具体场景，无需将所有分类类别标出，例：

- 三分类的口罩检测模型：FacemaskOD_
- 三分类的人、人头、头肩模型：PresonHS_OD（PersonHeadShoulder）
- 多分类的学校场景下检测模型：SchoolOD

注：提供多分类模型需要提供训练时的标签，顺序需准确无误。

### 2. 第二项：按照模型主干网络命名

根据模型主体网络使用的结构或框架命名，例：

- PersonOD_Yolov5s_
- FaceFeasE_Arcface_
- PersonKpD_Yolopose_
- FaceKpD_Retina_

### 3. 第三项：按照模型输入输出尺寸命名

根据模型的输入输出尺寸命名，例：

- PersonOD_Yolov5s_640_
- FaceFeasE_Arcface_112_
- PersonKpD_Yolopose_640_
- FaceKpD_Retina_640_

### 4. 第四项：按照模型数据集大小命名

根据模型训练时的数据集图片内标签数量命名，若为开源通用模型则无需注明，例：

- PersonOD_Yolov5s_640_300K_
- FaceKpD_Retina_640_32K_

### 5. 第五项：按照模型迭代时间命名

根据模型训练完毕时模型迭代的时间进行命名，若为开源通用模型则无需注明，例：

- PersonOD_Yolov5s_640_300K_230101.pt
- FacemaskOD_Yolov5s_640_17K_230214.pt
- FaceFeasE_Arcface_112.bmodel
- PersonKpD_Yolopose_640.onnx

注：非标准化通用模型在版本号后面注明特殊使用场景或用途。
