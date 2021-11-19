---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_VALIDATION_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_VALIDATION_FLAGS
ms.date: 06/10/2021
targetos: Windows
description: Flags specifying unsupported encoder features.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_VALIDATION_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_VALIDATION_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_VALIDATION_FLAGS
dev_langs:
 - c++
---

## -description

Specifies flags returned in the *ValidationFlags* field of the [D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT](ns-d3d12video-d3d12_feature_data_video_encoder_support.md) structure passed into a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_SUPPORT](ne-d3d12video-d3d12_feature_video.md). The returned flags indicate the features that are not supported.


## -enum-fields

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_CODEC_NOT_SUPPORTED

The specified codec is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_INPUT_FORMAT_NOT_SUPPORTED

The specified input format is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_CODEC_CONFIGURATION_NOT_SUPPORTED

The specified codec configuration is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_RATE_CONTROL_MODE_NOT_SUPPORTED

The specified rate control mode is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_RATE_CONTROL_CONFIGURATION_NOT_SUPPORTED

The specified rate control configuration is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_INTRA_REFRESH_MODE_NOT_SUPPORTED

The specified intra refresh mode is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_SUBREGION_LAYOUT_MODE_NOT_SUPPORTED

The specified subregion layout mode is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_RESOLUTION_NOT_SUPPORTED_IN_LIST

The specified resolution is not supported.

### -field D3D12_VIDEO_ENCODER_VALIDATION_FLAG_GOP_STRUCTURE_NOT_SUPPORTED

The specified GOP structure is not supported.

## -remarks

## -see-also

