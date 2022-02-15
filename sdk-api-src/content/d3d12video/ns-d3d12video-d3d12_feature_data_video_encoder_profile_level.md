---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
ms.date: 07/07/2021
targetos: Windows
description: Retrieves a value indicating if the specified profile is supported for video encoding.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_PROFILE_LEVEL
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_PROFILE_LEVEL](ne-d3d12video-d3d12_feature_video.md). Retrieves a value indicating if the specified profile is supported for video encoding.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which the supported profile level is being queried.

### -field Profile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) structure specifying the profile for which  support is being queried.

### -field IsSupported

Receives a boolean value indicating if the specified profile is supported for the specified codec.

### -field MinSupportedLevel

Output field that receives the minimum supported level for the selected codec and profile if supported.

### -field MaxSupportedLevel

Output field that receives the maximum supported level for the selected codec and profile if supported.

## -remarks

## -see-also

