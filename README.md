# oil-spill-segmentation
Classify and Segment Oil Spill in the Sea from Drone Footage<br>
<br>
![Oil Spill in Sea](https://github.com/tim3in/oil-spill-segmentation/blob/main/oil-spill-predection.jpg?raw=true)
<br><br>

Step 1: Run ``` oil_spill_instance_segmentation.ipynb ``` to train custom model<br>
Step 2: Inference using following code <br>
<br>
Inference on Image<br>
```python
from ultralytics import YOLO

model = YOLO("best.pt")
model.predict(source="oil_spill_drone.jpg", show=True, save=True, hide_labels=False, hide_conf=False, conf=0.5, save_txt=False, save_crop=False, line_thickness=2)
```

Inference on Video<br>
```python
from ultralytics import YOLO

model = YOLO("best.pt")
model.predict(source="drone_footage_oil_spill_original.mp4", show=True, save=True, hide_labels=False, hide_conf=False, conf=0.5, save_txt=False, save_crop=False, line_thickness=2)
```
