---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
ms.date: 06/07/2021
targetos: Windows
description: Retrieves a value indicating if the specified codec, profile, and format are supported for video encoding.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_INPUT_FORMAT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_INPUT_FORMAT](ne-d3d12video-d3d12_feature_video.md). Retrieves a value indicating if the specified codec, profile, and format are supported for video encoding.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which support is being queried.

### -field Profile

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the profile for which support is being queried.

### -field Format

A member of the [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) enumeration specifying the pixel format for which support is being queried. This format definition includes the subsampling and bit-depth modes settings for the video encoding session.

To query encoder support for 4:2:0 with 8 and 10 bitdepth samples using following values for the **Format** field:
- DXGI_FORMAT_P010
- DXGI_FORMAT_NV12

> [!NOTE]
> The host is expected to handle the input subsampling and color conversion stages of video encoding.

### -field IsSupported

Receives a boolean value indicating if the specified codec, profile, and format are supported.

## -remarks






## -see-also

