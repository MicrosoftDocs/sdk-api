---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
ms.date: 06/09/2021
targetos: Windows
description: Retrieves a value indicating if the specified codec configuration support parameters are supported for the provided HEVC encoding configuration or retrieves the supported configuration for H.264 encoding.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](ne-d3d12video-d3d12_feature_video.md). Retrieves a value indicating if the specified codec configuration support parameters are supported for the provided HEVC encoding configuration or retrieves the supported configuration for H.264 encoding.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which rate control mode support is being queried.

### -field Profile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) structure specifying the profile for which intra refresh mode support is being queried.

### -field IsSupported

Receives a boolean value indicating if the specified configuration parameters are supported for the specified codec.

### -field CodecSupportLimits

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT](ns-d3d12video-d3d12_video_encoder_codec_configuration_support.md) structure. For HEVC, the caller populates this structure with the desired encoder configuration. For H.264, the **CheckFeatureSupport** call populates the structure with the supported configuration.

## -remarks

## -see-also

