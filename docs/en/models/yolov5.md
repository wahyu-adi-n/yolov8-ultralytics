---
comments: true
description: Explore YOLOv5u, an advanced object detection model with optimized accuracy-speed tradeoff, featuring anchor-free Ultralytics head and various pre-trained models.
keywords: YOLOv5, YOLOv5u, object detection, Ultralytics, anchor-free, pre-trained models, accuracy, speed, real-time detection
---

# YOLOv5

## Overview

YOLOv5u represents an advancement in object detection methodologies. Originating from the foundational architecture of the [YOLOv5](https://github.com/ultralytics/yolov5) model developed by Ultralytics, YOLOv5u integrates the anchor-free, objectness-free split head, a feature previously introduced in the [YOLOv8](yolov8.md) models. This adaptation refines the model's architecture, leading to an improved accuracy-speed tradeoff in object detection tasks. Given the empirical results and its derived features, YOLOv5u provides an efficient alternative for those seeking robust solutions in both research and practical applications.

![Ultralytics YOLOv5](https://raw.githubusercontent.com/ultralytics/assets/main/yolov5/v70/splash.png)

## Key Features

- **Anchor-free Split Ultralytics Head:** Traditional object detection models rely on predefined anchor boxes to predict object locations. However, YOLOv5u modernizes this approach. By adopting an anchor-free split Ultralytics head, it ensures a more flexible and adaptive detection mechanism, consequently enhancing the performance in diverse scenarios.

- **Optimized Accuracy-Speed Tradeoff:** Speed and accuracy often pull in opposite directions. But YOLOv5u challenges this tradeoff. It offers a calibrated balance, ensuring real-time detections without compromising on accuracy. This feature is particularly invaluable for applications that demand swift responses, such as autonomous vehicles, robotics, and real-time video analytics.

- **Variety of Pre-trained Models:** Understanding that different tasks require different toolsets, YOLOv5u provides a plethora of pre-trained models. Whether you're focusing on Inference, Validation, or Training, there's a tailor-made model awaiting you. This variety ensures you're not just using a one-size-fits-all solution, but a model specifically fine-tuned for your unique challenge.

## Supported Tasks and Modes

The YOLOv5u models, with various pre-trained weights, excel in [Object Detection](../tasks/detect.md) tasks. They support a comprehensive range of modes, making them suitable for diverse applications, from development to deployment.

| Model Type | Pre-trained Weights                                                                                                         | Task                                   | Inference | Validation | Training | Export |
| ---------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- | --------- | ---------- | -------- | ------ |
| YOLOv5u    | `yolov5nu`, `yolov5su`, `yolov5mu`, `yolov5lu`, `yolov5xu`, `yolov5n6u`, `yolov5s6u`, `yolov5m6u`, `yolov5l6u`, `yolov5x6u` | [Object Detection](../tasks/detect.md) | ✅        | ✅         | ✅       | ✅     |

This table provides a detailed overview of the YOLOv5u model variants, highlighting their applicability in object detection tasks and support for various operational modes such as [Inference](../modes/predict.md), [Validation](../modes/val.md), [Training](../modes/train.md), and [Export](../modes/export.md). This comprehensive support ensures that users can fully leverage the capabilities of YOLOv5u models in a wide range of object detection scenarios.

## Performance Metrics

!!! Performance

    === "Detection"

    See [Detection Docs](../tasks/detect.md) for usage examples with these models trained on [COCO](../datasets/detect/coco.md), which include 80 pre-trained classes.

    | Model                                                                                       | YAML                                                                                                           | size<br><sup>(pixels) | mAP<sup>val<br>50-95 | Speed<br><sup>CPU ONNX<br>(ms) | Speed<br><sup>A100 TensorRT<br>(ms) | params<br><sup>(M) | FLOPs<br><sup>(B) |
    |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------|----------------------|--------------------------------|-------------------------------------|--------------------|-------------------|
    | [yolov5nu.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5nu.pt)   | [yolov5n.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5.yaml)     | 640                   | 34.3                 | 73.6                           | 1.06                                | 2.6                | 7.7               |
    | [yolov5su.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5su.pt)   | [yolov5s.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5.yaml)     | 640                   | 43.0                 | 120.7                          | 1.27                                | 9.1                | 24.0              |
    | [yolov5mu.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5mu.pt)   | [yolov5m.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5.yaml)     | 640                   | 49.0                 | 233.9                          | 1.86                                | 25.1               | 64.2              |
    | [yolov5lu.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5lu.pt)   | [yolov5l.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5.yaml)     | 640                   | 52.2                 | 408.4                          | 2.50                                | 53.2               | 135.0             |
    | [yolov5xu.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5xu.pt)   | [yolov5x.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5.yaml)     | 640                   | 53.2                 | 763.2                          | 3.81                                | 97.2               | 246.4             |
    |                                                                                             |                                                                                                                |                       |                      |                                |                                     |                    |                   |
    | [yolov5n6u.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5n6u.pt) | [yolov5n6.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5-p6.yaml) | 1280                  | 42.1                 | 211.0                          | 1.83                                | 4.3                | 7.8               |
    | [yolov5s6u.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5s6u.pt) | [yolov5s6.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5-p6.yaml) | 1280                  | 48.6                 | 422.6                          | 2.34                                | 15.3               | 24.6              |
    | [yolov5m6u.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5m6u.pt) | [yolov5m6.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5-p6.yaml) | 1280                  | 53.6                 | 810.9                          | 4.36                                | 41.2               | 65.7              |
    | [yolov5l6u.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5l6u.pt) | [yolov5l6.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5-p6.yaml) | 1280                  | 55.7                 | 1470.9                         | 5.47                                | 86.1               | 137.4             |
    | [yolov5x6u.pt](https://github.com/ultralytics/assets/releases/download/v8.2.0/yolov5x6u.pt) | [yolov5x6.yaml](https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v5/yolov5-p6.yaml) | 1280                  | 56.8                 | 2436.5                         | 8.98                                | 155.4              | 250.7             |

## Usage Examples

This example provides simple YOLOv5 training and inference examples. For full documentation on these and other [modes](../modes/index.md) see the [Predict](../modes/predict.md), [Train](../modes/train.md), [Val](../modes/val.md) and [Export](../modes/export.md) docs pages.

!!! Example

    === "Python"

        PyTorch pretrained `*.pt` models as well as configuration `*.yaml` files can be passed to the `YOLO()` class to create a model instance in python:

        ```python
        from ultralytics import YOLO

        # Load a COCO-pretrained YOLOv5n model
        model = YOLO("yolov5n.pt")

        # Display model information (optional)
        model.info()

        # Train the model on the COCO8 example dataset for 100 epochs
        results = model.train(data="coco8.yaml", epochs=100, imgsz=640)

        # Run inference with the YOLOv5n model on the 'bus.jpg' image
        results = model("path/to/bus.jpg")
        ```

    === "CLI"

        CLI commands are available to directly run the models:

        ```bash
        # Load a COCO-pretrained YOLOv5n model and train it on the COCO8 example dataset for 100 epochs
        yolo train model=yolov5n.pt data=coco8.yaml epochs=100 imgsz=640

        # Load a COCO-pretrained YOLOv5n model and run inference on the 'bus.jpg' image
        yolo predict model=yolov5n.pt source=path/to/bus.jpg
        ```

## Citations and Acknowledgements

If you use YOLOv5 or YOLOv5u in your research, please cite the Ultralytics YOLOv5 repository as follows:

!!! Quote ""

    === "BibTeX"

        ```bibtex
        @software{yolov5,
          title = {Ultralytics YOLOv5},
          author = {Glenn Jocher},
          year = {2020},
          version = {7.0},
          license = {AGPL-3.0},
          url = {https://github.com/ultralytics/yolov5},
          doi = {10.5281/zenodo.3908559},
          orcid = {0000-0001-5950-6979}
        }
        ```

Please note that YOLOv5 models are provided under [AGPL-3.0](https://github.com/ultralytics/ultralytics/blob/main/LICENSE) and [Enterprise](https://ultralytics.com/license) licenses.

## FAQ

### What is YOLOv5u and how does it differ from YOLOv5?

YOLOv5u is an advanced version of the YOLOv5 object detection model developed by Ultralytics. It introduces an anchor-free, objectness-free split head, a feature adopted from the YOLOv8 models. This architectural change enhances the model's accuracy-speed tradeoff, making it more efficient and flexible for various object detection tasks. Learn more about these features in the [YOLOv5 Overview](#overview).

### Why should I use the anchor-free split head in YOLOv5u?

The anchor-free split head in YOLOv5u offers several advantages:

- **Flexibility:** It alleviates the need for predefined anchor boxes, making the model more adaptable to diverse object scales and shapes.
- **Simplicity:** Reducing dependencies on anchor boxes simplifies the model architecture, potentially decreasing the computational load.
- **Performance:** Empirical results show enhanced performance in terms of accuracy and speed, making it suitable for real-time applications.

For detailed information, see the [Anchor-free Split Ultralytics Head section](#key-features).

### How can I deploy the YOLOv5u model for real-time object detection?

Deploying YOLOv5u for real-time object detection involves several steps:

1. **Load the Model:**

    ```python
    from ultralytics import YOLO

    model = YOLO("yolov5u.pt")
    ```

2. **Run Inference:**
    ```python
    results = model("path/to/image.jpg")
    ```

For a comprehensive guide, refer to the [Usage Examples](#usage-examples) section.

### What are the pre-trained model variants available for YOLOv5u?

YOLOv5u offers a variety of pre-trained models to cater to different needs:

- **YOLOv5nu**
- **YOLOv5su**
- **YOLOv5mu**
- **YOLOv5lu**
- **YOLOv5xu**
- **YOLOv5n6u**
- **YOLOv5s6u**
- **YOLOv5m6u**
- **YOLOv5l6u**
- **YOLOv5x6u**

These models support tasks like detection and offer various modes such as [Inference](../modes/predict.md), [Validation](../modes/val.md), [Training](../modes/train.md), and [Export](../modes/export.md). For detailed metrics, see the [Performance Metrics](#performance-metrics) section.

### How do YOLOv5u models perform on different hardware setups?

YOLOv5u models have been evaluated on both CPU and GPU hardware, demonstrating competitive performance metrics across various setups. For example:

- **YOLOv5nu.pt:**

    - **Speed (CPU ONNX):** 73.6 ms
    - **Speed (A100 TensorRT):** 1.06 ms
    - **mAP (50-95):** 34.3

- **YOLOv5lu.pt:**
    - **Speed (CPU ONNX):** 408.4 ms
    - **Speed (A100 TensorRT):** 2.50 ms
    - **mAP (50-95):** 52.2

For more detailed performance metrics, visit the [Performance Metrics](#performance-metrics) section.
