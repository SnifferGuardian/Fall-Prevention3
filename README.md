# THIS IS NOT MINE




[简体中文](README_CN.md) | [English](README.md)



# RKNN Model Zoo

## Description

`RKNN Model Zoo` is developed based on the RKNPU SDK toolchain and provides deployment examples for current mainstream algorithms. Include the process of `exporting the RKNN model` and using `Python API` and `CAPI` to infer the RKNN model.

- Support `RK3562`, `RK3566`, `RK3568`, `RK3576`, `RK3588` , `RV1126B`  platforms. 
- Limited support `RV1103`, `RV1106` 
- Support  `RV1109`, `RV1126`, `RK1808` platforms.



## Dependency library installation

`RKNN Model Zoo` relies on `RKNN-Toolkit2` for model conversion. The Android compilation tool chain is required when compiling the Android demo, and the Linux compilation tool chain is required when compiling the Linux demo. For the installation of these dependencies, please refer to the `Quick Start` documentation at https://github.com/airockchip/rknn-toolkit2/tree/master/doc.

- Please note that the Android compilation tool chain recommends using `version r18 or r19`. Using other versions may encounter the problem of Cdemo compilation failure.
- Please note that the Linux compilation tool chain recommends using `gcc-linaro-6.3.1(aarch64)/gcc-arm-8.3(armhf)/armhf-uclibcgnueabihf(armhf for RV1106/RV1103 series)`. Using other versions may encounter the problem of Cdemo compilation failure. For detailed compilation guide, please refer to [Compilation_Environment_Setup_Guide.md](./docs/Compilation_Environment_Setup_Guide.md)


## Model support

In addition to exporting the model from the corresponding respository, the models file are available on https://console.zbox.filez.com/l/8ufwtG (key: rknn). 

| Category | Name | Dtype | Model Download Link | Support platform |
| --- | --- | --- | --- | --- |
| Classification | [mobilenet](https://github.com/onnx/models/tree/8e893eb39b131f6d3970be6ebd525327d3df34ea/vision/classification/mobilenet/model/mobilenetv2-12.onnx) | FP16/INT8 | [mobilenetv2-12.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/mobilenet/mobilenetv2-12.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RV1103\|RV1106<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Classification | [resnet](https://github.com/onnx/models/tree/8e893eb39b131f6d3970be6ebd525327d3df34ea/vision/classification/resnet/model/resnet50-v2-7.onnx) | FP16/INT8 | [resnet50-v2-7.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/resnet/resnet50-v2-7.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov5](https://github.com/airockchip/yolov5) | FP16/INT8 | [./yolov5s_relu.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5/yolov5s_relu.onnx)<br/>[./yolov5n.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5/yolov5n.onnx)<br/>[./yolov5s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5/yolov5s.onnx)<br/>[./yolov5m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5/yolov5m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RV1103\|RV1106<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov6](https://github.com/airockchip/yolov6) | FP16/INT8 | [./yolov6n.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov6/yolov6n.onnx)<br/>[./yolov6s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov6/yolov6s.onnx)<br/>[./yolov6m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov6/yolov6m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov7](https://github.com/airockchip/yolov7) | FP16/INT8 | [./yolov7-tiny.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov7/yolov7-tiny.onnx)<br/>[./yolov7.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov7/yolov7.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov8](https://github.com/airockchip/ultralytics_yolov8) | FP16/INT8 | [./yolov8n.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8/yolov8n.onnx)<br/>[./yolov8s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8/yolov8s.onnx)<br/>[./yolov8m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8/yolov8m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov8_obb](https://github.com/airockchip/ultralytics_yolov8) | INT8 | [./yolov8n-obb.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8_obb/yolov8n-obb.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolov10](https://github.com/THU-MIG/yolov10) | FP16/INT8 | [./yolov10n.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov10/yolov10n.onnx)<br/>[./yolov10s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov10/yolov10s.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RV1103\|RV1106<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolo11](https://github.com/airockchip/ultralytics_yolo11) | FP16/INT8 | [./yolo11n.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolo11/yolo11n.onnx)<br/>[./yolo11s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolo11/yolo11s.onnx)<br/>[./yolo11m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolo11/yolo11m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RV1103\|RV1106<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolox](https://github.com/airockchip/YOLOX) | FP16/INT8 | [./yolox_s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolox/yolox_s.onnx)<br/>[./yolox_m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolox/yolox_m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [ppyoloe](https://github.com/PaddlePaddle/PaddleDetection/blob/release/2.6/configs/ppyoloe) | FP16/INT8 | [./ppyoloe_s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/ppyoloe/ppyoloe_s.onnx)<br/>[./ppyoloe_m.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/ppyoloe/ppyoloe_m.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Object Detection | [yolo_world](https://github.com/AILab-CVC/YOLO-World) | FP16/INT8 | [./yolo_world_v2s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolo_world/yolo_world_v2s.onnx)<br/>[./clip_text.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolo_world/clip_text.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |
| Body Pose | [yolov8_pose](https://github.com/airockchip/ultralytics_yolov8) | INT8 | [./yolov8n-pose.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8_pose/yolov8n-pose.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |
| Image Segmentation | deeplabv3 | FP16/INT8 | [./deeplab-v3-plus-mobilenet-v2.pb](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/deeplabv3/deeplab-v3-plus-mobilenet-v2.pb) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Image Segmentation | [yolov5_seg](https://github.com/airockchip/yolov5) | FP16/INT8 | [./yolov5n-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5_seg/yolov5n-seg.onnx)<br/>[./yolov5s-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5_seg/yolov5s-seg.onnx)<br/>[./yolov5m-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov5_seg/yolov5m-seg.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Image Segmentation | [yolov8_seg](https://github.com/airockchip/ultralytics_yolov8) | FP16/INT8 | [./yolov8n-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8_seg/yolov8n-seg.onnx)<br/>[./yolov8s-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8_seg/yolov8s-seg.onnx)<br/>[./yolov8m-seg.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yolov8_seg/yolov8m-seg.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Image Segmentation | [ppseg](https://github.com/PaddlePaddle/PaddleSeg/tree/release/2.8) | FP16/INT8 | [pp_liteseg_cityscapes.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/ppseg/pp_liteseg_cityscapes.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Image Segmentation | [mobilesam](https://github.com/ChaoningZhang/MobileSAM) | FP16 | [mobilesam_encoder_tiny.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/mobilesam/mobilesam_encoder_tiny.onnx)<br />[mobilesam_decoder.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/mobilesam/mobilesam_decoder.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B |
| Face Key Points | [RetinaFace](https://github.com/biubug6/Pytorch_Retinaface) | INT8 | [RetinaFace_mobile320.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/RetinaFace/RetinaFace_mobile320.onnx)<br/>[RetinaFace_resnet50_320.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/RetinaFace/RetinaFace_resnet50_320.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Car Plate Recognition | [LPRNet](https://github.com/sirius-ai/LPRNet_Pytorch/) | FP16/INT8 | [./lprnet.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/LPRNet/lprnet.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RV1103\|RV1106<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Text Detection | [PPOCR-Det](https://github.com/PaddlePaddle/PaddleOCR/tree/release/2.7) | FP16/INT8 | [../ppocrv4_det.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/PPOCR/ppocrv4_det.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Text Recognition | [PPOCR-Rec](https://github.com/PaddlePaddle/PaddleOCR/tree/release/2.7) | FP16 | [../ppocrv4_rec.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/PPOCR/ppocrv4_rec.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Neural Machine Translation | [lite_transformer](https://github.com/airockchip/lite-transformer) | FP16 | [lite-transformer-encoder-16.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/lite_transformer/lite-transformer-encoder-16.onnx)<br/>[lite-transformer-decoder-16.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/lite_transformer/lite-transformer-decoder-16.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/>RK1808\|RK3399PRO<br/>RV1109\|RV1126 |
| Image-Text Matching | [clip](https://huggingface.co/openai/clip-vit-base-patch32) | FP16 | [./clip_images.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/clip/clip_images.onnx)<br/>[./clip_text.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/clip/clip_text.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |
| Speech Recognition | [wav2vec2](https://github.com/facebookresearch/fairseq/tree/main/examples/wav2vec#wav2vec-20) | FP16 | [wav2vec2_base_960h_20s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/wav2vec2/wav2vec2_base_960h_20s.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B |
| Speech Recognition | [whisper](https://github.com/openai/whisper) | FP16 | [whisper_encoder_base_20s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/whisper/whisper_encoder_base_20s.onnx)<br/>[whisper_decoder_base_20s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/whisper/whisper_decoder_base_20s.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |
| Speech Recognition | [zipformer](https://huggingface.co/csukuangfj/k2fsa-zipformer-bilingual-zh-en-t) | FP16 | [encoder-epoch-99-avg-1.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/zipformer/encoder-epoch-99-avg-1.onnx)<br/>[decoder-epoch-99-avg-1.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/zipformer/decoder-epoch-99-avg-1.onnx)<br/>[joiner-epoch-99-avg-1.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/zipformer/joiner-epoch-99-avg-1.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |
| Speech Classification | [yamnet](https://www.tensorflow.org/hub/tutorials/yamnet) | FP16 | [yamnet_3s.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/yamnet/yamnet_3s.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B |
| Text to Speech | [mms_tts](https://huggingface.co/facebook/mms-tts-eng) | FP16 | [mms_tts_eng_encoder_200.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/mms_tts/mms_tts_eng_encoder_200.onnx)<br/>[mms_tts_eng_decoder_200.onnx](https://ftrg.zbox.filez.com/v2/delivery/data/95f00b0fc900458ba134f8b180b3f7a1/examples/mms_tts/mms_tts_eng_decoder_200.onnx) | RK3562\|RK3566\|RK3568\|RK3576\|RK3588\|RV1126B<br/> |




## Model performance benchmark(FPS)

| demo             | model_name                          | inputs_shape&nbsp;&nbsp;&nbsp;&nbsp; | dtype | RK3566<br />RK3568 | RK3562         | RK3588<br />@single_core | RK3576<br />@single_core | RV1109     | RV1126     | RK1808     |
| ---------------- | ----------------------------------- | ------------------------------------ | ----- | ------------------ | -------------- | ------------------------ | ------------------------ | ---------- | ---------- | ---------- |
| mobilenet        | mobilenetv2-12                      | [1, 3, 224, 224]        | INT8     | 180.7                 | 281.3     | 450.7          | 467.0     | 212.9      | 322.3      | 170.3      |
| resnet           | resnet50-v2-7                       | [1, 3, 224, 224]        | INT8     | 37.9                  | 54.9      | 110.1          | 99.0      | 24.4       | 36.2       | 37.1       |
| yolov5           | yolov5s_relu                        | [1, 3, 640, 640]        | INT8     | 25.5                  | 33.2      | 66.1           | 65.0      | 20.2       | 29.2       | 37.2       |
|                  | yolov5n                             | [1, 3, 640, 640]        | INT8     | 39.7                  | 47.4      | 82.5           | 112.7     | 36.3       | 53.2       | 61.2       |
|                  | yolov5s                             | [1, 3, 640, 640]        | INT8     | 19.3                  | 23.6      | 48.4           | 57.5      | 13.6       | 20.0       | 28.2       |
|                  | yolov5m                             | [1, 3, 640, 640]        | INT8     | 8.6                   | 10.8      | 20.9           | 23.7      | 5.8        | 8.5        | 13.3       |
| yolov6           | yolov6n                             | [1, 3, 640, 640]        | INT8     | 48.8                  | 56.4      | 106.4          | 109.1     | 37.8       | 56.8       | 66.8       |
|                  | yolov6s                             | [1, 3, 640, 640]        | INT8     | 15.2                  | 17.3      | 36.4           | 35.0      | 10.8       | 16.3       | 24.1       |
|                  | yolov6m                             | [1, 3, 640, 640]        | INT8     | 7.2                   | 8.6       | 17.8           | 17.4      | 5.6        | 8.3        | 11.5       |
| yolov7           | yolov7-tiny                         | [1, 3, 640, 640]        | INT8     | 27.9                  | 36.5      | 72.7           | 74.8      | 15.4       | 22.4       | 37.2       |
|                  | yolov7                              | [1, 3, 640, 640]        | INT8     | 4.6                   | 5.9       | 11.4           | 13.0      | 3.3        | 4.8        | 7.4        |
| yolov8           | yolov8n                             | [1, 3, 640, 640]        | INT8     | 34.0                  | 40.9      | 73.5           | 90.2      | 24.0       | 35.4       | 42.3       |
|                  | yolov8s                             | [1, 3, 640, 640]        | INT8     | 15.1                  | 18.4      | 38.0           | 40.8      | 8.9        | 13.1       | 19.1       |
|                  | yolov8m                             | [1, 3, 640, 640]        | INT8     | 6.5                   | 8.2       | 16.2           | 16.7      | 3.9        | 5.8        | 9.1        |
| yolov8_obb       | yolov8n-obb                         | [1, 3, 640, 640]        | INT8     | 33.9                  | 41.3      | 74.0           | 90.2      | 25.1       | 37.3       | 42.8       |
| yolov10          | yolov10n                            | [1, 3, 640, 640]        | INT8     | 20.7                  | 34.1      | 61.2           | 80.2      | /          | /          | /          |
|                  | yolov10s                            | [1, 3, 640, 640]        | INT8     | 10.3                  | 16.9      | 33.8           | 39.9      | /          | /          | /          |
| yolo11           | yolo11n                             | [1, 3, 640, 640]        | INT8     | 20.6                  | 34.0      | 60.0           | 77.9      | 11.7       | 17.0       | 17.6       |
|                  | yolo11s                             | [1, 3, 640, 640]        | INT8     | 10.2                  | 16.7      | 33.0           | 38.2      | 5.0        | 7.3        | 8.4        |
|                  | yolo11m                             | [1, 3, 640, 640]        | INT8     | 4.6                   | 6.5       | 12.7           | 14.6      | 2.8        | 4.0        | 5.1        |
| yolox            | yolox_s                             | [1, 3, 640, 640]        | INT8     | 15.2                  | 18.3      | 37.1           | 41.5      | 10.6       | 15.7       | 23.0       |
|                  | yolox_m                             | [1, 3, 640, 640]        | INT8     | 6.6                   | 8.2       | 16.0           | 17.6      | 4.6        | 6.8        | 10.7       |
| ppyoloe          | ppyoloe_s                           | [1, 3, 640, 640]        | INT8     | 17.1                   | 20.0      | 32.5           | 41.3      | 11.2       | 16.4       | 21.1       |
|                  | ppyoloe_m                           | [1, 3, 640, 640]        | INT8     | 7.8                   | 9.2       | 15.8           | 17.8      | 5.2        | 7.7        | 9.4        |
| yolo_world       | yolo_world_v2s                      | [1, 3, 640, 640]        | INT8     | 7.4                   | 9.6       | 22.1           | 22.3      | /          | /          | /          |
|                  | clip_text                           | [1, 20]                 | FP16     | 29.8                  | 67.4      | 95.8           | 63.5      | /          | /          | /          |
| yolov8_pose      | yolov8n-pose                        | [1, 3, 640, 640]        | INT8     | 22.6                  | 31.0      | 55.9           | 66.8      | /          | /          | /          |
| deeplabv3        | deeplab-v3-plus-mobilenet-v2        | [1, 513, 513, 1]        | INT8     | 10.9                  | 21.4      | 34.0           | 39.4      | 10.1       | 13.0       | 4.4        |
| yolov5_seg       | yolov5n-seg                         | [1, 3, 640, 640]        | INT8     | 32.2                  | 38.5      | 69.3           | 88.3      | 28.6       | 42.2       | 49.6       |
|                  | yolov5s-seg                         | [1, 3, 640, 640]        | INT8     | 15.0                  | 18.1      | 36.8           | 41.6      | 9.6        | 14.0       | 22.5       |
|                  | yolov5m-seg                         | [1, 3, 640, 640]        | INT8     | 6.8                   | 8.4       | 16.4           | 18.0      | 4.7        | 6.8        | 10.8       |
| yolov8_seg       | yolov8n-seg                         | [1, 3, 640, 640]        | INT8     | 27.8                  | 33.0      | 60.8           | 71.1      | 18.6       | 27.6       | 32.9       |
|                  | yolov8s-seg                         | [1, 3, 640, 640]        | INT8     | 11.7                  | 14.1      | 28.9           | 30.8      | 6.6        | 9.8        | 14.6       |
|                  | yolov8m-seg                         | [1, 3, 640, 640]        | INT8     | 5.2                   | 6.4       | 12.6           | 12.7      | 3.1        | 4.6        | 6.9        |
| ppseg            | ppseg_lite_1024x512                 | [1, 3, 512, 512]        | INT8     | 5.9                   | 13.9      | 35.7           | 33.6      | 18.4       | 27.1       | 20.9       |
| mobilesam        | mobilesam_encoder_tiny              | [1, 3, 448, 448]        | FP16     | 1.0                   | 6.6       | 10.0           | 11.9      | /          | /          | /          |
|                  | mobilesam_decoder                   | [1, 1, 112, 112]        | FP16     | 24.3                  | 69.6      | 116.4          | 108.6     | /          | /          | /          |
| RetinaFace       | RetinaFace_mobile320                | [1, 3, 320, 320]        | INT8     | 156.4                 | 300.8     | 227.2          | 470.5     | 144.8      | 212.5      | 198.5      |
|                  | RetinaFace_resnet50_320             | [1, 3, 320, 320]        | INT8     | 18.7                  | 26.9      | 49.2           | 56.6      | 14.6       | 20.8       | 24.6       |
| LPRNet           | lprnet                              | [1, 3, 24, 94]          | FP16     | 143.2                 | 420.6     | 586.4          | 647.8     | 30.6(INT8) | 47.6(INT8) | 30.1(INT8) |
| PPOCR-Det        | ppocrv4_det                         | [1, 3, 480, 480]        | INT8     | 22.1                  | 28.0      | 50.7           | 64.3      | 11.0       | 16.1       | 14.2       |
| PPOCR-Rec        | ppocrv4_rec                         | [1, 3, 48, 320]         | FP16     | 19.5                  | 54.3      | 73.9           | 96.8      | 1.0        | 1.6        | 6.7        |
| lite_transformer | lite-transformer-encoder-16         | embedding-256, token-16 | FP16     | 337.5                 | 725.8     | 867.6          | 784.1     | 22.7       | 35.4       | 98.3       |
|                  | lite-transformer-decoder-16         | embedding-256, token-16 | FP16     | 142.5                 | 252.0     | 343.8          | 272.3     | 48.0       | 65.8       | 109.9      |
| clip             | clip_images                         | [1, 3, 224, 224]        | FP16     | 2.3                   | 3.4       | 6.5            | 6.7       | /          | /          | /          |
|                  | clip_text                           | [1, 20]                 | FP16     | 29.7                  | 66.6      | 96.0           | 63.7      | /          | /          | /          |
| wav2vec2         | wav2vec2_base_960h_20s              | 20s audio               | FP16     | RTF <br>0.817   | RTF <br>0.323   | RTF <br>0.133  | RTF <br>0.073  | /        | /        | /         |
| whisper          | whisper_base_20s                    | 20s audio               | FP16     | RTF <br>1.178   | RTF <br>0.420   | RTF <br>0.215  | RTF <br>0.218  | /        | /        | /         |
| zipformer        | zipformer-bilingual-zh-en-t         | streaming audio         | FP16     | RTF <br>0.196   | RTF <br>0.116   | RTF <br>0.065  | RTF <br>0.082  | /        | /        | /         |
| yamnet           | yamnet_3s                           | 3s audio                | FP16     | RTF <br>0.013   | RTF <br>0.008   | RTF <br>0.004  | RTF <br>0.005  | /        | /        | /         |
| mms_tts          | mms_tts_eng_200                     | token-200               | FP16     | RTF <br>0.311   | RTF <br>0.138   | RTF <br>0.069  | RTF <br>0.069  | /        | /        | /         |

- This performance data are collected based on the maximum NPU frequency of each platform.
- This performance data calculate the time-consuming of model inference. Does not include the time-consuming of pre-processing and post-processing if not specified.
- `/` means currently not support.



## Compile Demo

For Linux develop board:

```sh
./build-linux.sh -t <target> -a <arch> -d <build_demo_name> [-b <build_type>] [-m]
    -t : target (rk356x/rk3576/rk3588/rv1106/rv1126b/rv1126/rk1808)
    -a : arch (aarch64/armhf)
    -d : demo name
    -b : build_type(Debug/Release)
    -m : enable address sanitizer, build_type need set to Debug
Note: 'rk356x' represents rk3562/rk3566/rk3568, 'rv1106' represents rv1103/rv1106, 'rv1126' represents rv1109/rv1126，'rv1126b' is different from 'rv1126'.

# Here is an example for compiling yolov5 demo for 64-bit Linux RK3566.
./build-linux.sh -t rk356x -a aarch64 -d yolov5
```

For Android development board:

```sh
# For Android develop boards, it's require to set path for Android NDK compilation tool path according to the user environment
export ANDROID_NDK_PATH=~/opts/ndk/android-ndk-r18b
./build-android.sh -t <target> -a <arch> -d <build_demo_name> [-b <build_type>] [-m]
    -t : target (rk356x/rk3576/rk3588)
    -a : arch (arm64-v8a/armeabi-v7a)
    -d : demo name
    -b : build_type (Debug/Release)
    -m : enable address sanitizer, build_type need set to Debug

# Here is an example for compiling yolov5 demo for 64-bit Android RK3566.
./build-android.sh -t rk356x -a arm64-v8a -d yolov5
```



## Release Notes

| Version | Description                                                  |
| ------- | ------------------------------------------------------------ |
| 2.3.2   | Add support for `RV1126B`. |
| 2.3.0   | New demos released, including yolo11, zipformer, mms_tts, etc. |
| 2.2.0   | New demo wav2vec, mobilesam release. Update demo guide about exporting model. |
| 2.1.0   | New demo release, including yolov8_pose, yolov8_obb, yolov10, yolo_world, clip, whisper, yamnet<br>`RK1808`, `RV1109`, `RV1126` platform support of these demo will be added in next version. |
| 2.0.0   | Add support for `RK3576`.<br />Add support for `RK1808`,  `RV1109`, `RV1126`. |
| 1.6.0   | New demo release, including object detection, image segmentation, OCR, car plate detection&recognition etc.<br />Full support for `RK3566`, `RK3568`, `RK3588`, `RK3562` platforms.<br />Limited support for `RV1103`, `RV1106` platforms. |
| 1.5.0   | Yolo detection demo release.                                 |



## Environment dependencies

All demos in `RKNN Model Zoo` are verified based on the latest RKNPU SDK. If using a lower version for verification, the inference performance and inference results may be wrong.

| Version | RKNPU2 SDK | RKNPU1 SDK |
| ------- | ---------- | ---------- |
| 2.3.2   | >=2.3.2    | >=1.7.5    |
| 2.3.0   | >=2.3.0    | >=1.7.5    |
| 2.2.0   | >=2.2.0    | >=1.7.5    |
| 2.1.0   | >=2.1.0    | >=1.7.5    |
| 2.0.0   | >=2.0.0    | >=1.7.5    |
| 1.6.0   | >=1.6.0    | -          |
| 1.5.0   | >=1.5.0    | >=1.7.3    |



## RKNPU Resource

- RKNPU2 SDK: https://github.com/airockchip/rknn-toolkit2
- RKNPU1 SDK: https://github.com/airockchip/rknn-toolkit



## License

[Apache License 2.0](./LICENSE)

