---
title: MLCameraResultExtras
---

# MLCameraResultExtras

**Module:** **[Camera](/api-ref/api/Modules/group___camera/group___camera.md)**



 [More...](#detailed-description)


`#include <ml_camera_v2.h>`

## Public Attributes

| Type           | Name           |
| -------------- | -------------- |
| uint32_t | **[version](/api-ref/api/Modules/group___camera/struct_m_l_camera_result_extras.md#uint32-t-version)**  |
| int64_t | **[frame_number](/api-ref/api/Modules/group___camera/struct_m_l_camera_result_extras.md#int64-t-frame-number)**  |
| [MLTime](/api-ref/api/Modules/group___common/group___common.md#int64-t-mltime) | **[vcam_timestamp](/api-ref/api/Modules/group___camera/struct_m_l_camera_result_extras.md#mltime-vcam-timestamp)**  |
| [MLCameraIntrinsicCalibrationParameters](/api-ref/api/Modules/group___camera/struct_m_l_camera_intrinsic_calibration_parameters.md) * | **[intrinsics](/api-ref/api/Modules/group___camera/struct_m_l_camera_result_extras.md#mlcameraintrinsiccalibrationparameters-intrinsics)**  |

## Detailed Description

```cpp
struct MLCameraResultExtras;
```


A structure to encapsulate various indices for a capture result. 
#
-----------
## Public Attributes Documentation

### version {#uint32-t-version}

```cpp
uint32_t version;
```


Version of this structure. 
#
-----------

### frame_number {#int64-t-frame-number}

```cpp
int64_t frame_number;
```


A 64bit integer to index the frame number associated with this result. 
#
-----------

### vcam_timestamp {#mltime-vcam-timestamp}

```cpp
MLTime vcam_timestamp;
```


Frame timestamp. 
#
-----------

### intrinsics {#mlcameraintrinsiccalibrationparameters-intrinsics}

```cpp
MLCameraIntrinsicCalibrationParameters * intrinsics;
```



| Type | Description |
|--|--|
| [MLCameraIntrinsicCalibrationParameters](/api-ref/api/Modules/group___camera/struct_m_l_camera_intrinsic_calibration_parameters.md) * | Camera intrinsic parameter.  |


Camera intrinsic parameter.

Only valid within callback scope.

The Library allocates and maintains the lifetime of intrinsics.

Only valid when camera connected with MLCameraConnectFlag_CamOnly flag.

Only valid for on_image_buffer_available, on_video_buffer_available, on_preview_buffer_available callbacks.

NULL for on_capture_completed, on_capture_failed callbacks. 
#
-----------

