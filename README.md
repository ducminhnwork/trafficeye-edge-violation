# TrafficEye Edge

Traffic camera that counts vehicles and detects violations on the edge, sending only events and blurred evidence to a central dashboard.

> Status: in progress

## Pipeline

```
Data -> Augmentation -> Train YOLOv8-nano -> Export ONNX/TensorRT
-> Edge app: YOLO -> ByteTrack -> violation rules -> plate OCR -> blur evidence
-> MQTT / FastAPI -> Central dashboard (2 roles, human review) -> Evaluation
```

## Apps

- **Edge**: video, vehicle counts, FPS, violation alerts. Works offline.
- **Central**: web dashboard for operator and admin/traffic police.

Edge hardware is simulated on a laptop (limited CPU/RAM).

## Tech stack

YOLOv8-nano · ByteTrack · ONNX/TensorRT · OCR · FastAPI · React · MQTT

## Run

_Coming soon._
