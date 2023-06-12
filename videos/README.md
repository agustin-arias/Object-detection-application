# Real-Time Object Detection Model

This is an object detection model that performs real-time object detection on videos. It uses a pre-trained deep learning model to detect objects in each frame of a video stream.

## Model Description

The model is based on the MobileNet Single Shot MultiBox Detector (SSD) architecture. It is trained on the COCO (Common Objects in Context) dataset, which consists of various object categories. The model can detect objects such as people, cars, animals, and common household items.

## Requirements

- Python 3.7 or higher
- OpenCV 4.5 or higher
- imutils
- numpy

## Usage

1. Clone the repository:

```
  git clone https://github.com/agustinntarias/real-time-object-detection.git
```

2. Install the required dependencies:

```
pip install -r requirements.txt
```

3. Download the pre-trained model and prototxt file:

   - [MobileNet SSD Caffe Model](https://github.com/chuanqi305/MobileNet-SSD)
   - [MobileNet SSD Caffe Prototxt](https://github.com/chuanqi305/MobileNet-SSD)

4. Place the downloaded model and prototxt file in the project directory.

5. Run the real-time object detection script:

```
python real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt --model MobileNetSSD_deploy.caffemodel --video path/to/video/file.mp4
```

Replace `path/to/video/file.mp4` with the path to your video file.

6. The script will open a window displaying the video stream with bounding boxes and labels around detected objects. Press 'q' to quit the application.

## Customization

- Minimum Confidence Threshold: You can adjust the minimum confidence threshold for object detection by modifying the `--confidence` argument when running the script. The default value is 0.2.

- Supported Classes: The model can detect a range of objects defined by the COCO dataset. The list of supported classes can be found in the `CLASSES` variable in the `real_time_object_detection.py` script. You can modify this list to include or exclude specific classes based on your application's needs.

## License

This project is licensed under the [MIT License](LICENSE).
