# YOLOv5-Lite-NCNN-Deployment-Guide

```
git clone https://github.com/ppogg/YOLOv5-Lite.git
```

```
pip install -r requirements.txt
```
```CMakeLists
set(ncnn_DIR "/home/ncnn/build/install/lib/cmake/ncnn")
```

```cpp
#if USE_INT8
    yolov5.opt.use_int8_inference=true;
#else
    // yolov5.opt.use_vulkan_compute = true; << comment out
    // yolov5.opt.use_bf16_storage = true; << comment out
#endif
```

```cpp
yolov5.load_param("../model_zoo/v5lite-s.param");
yolov5.load_model("../model_zoo/v5lite-s.bin");
```
