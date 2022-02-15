---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
ms.date: 06/07/2021
targetos: Windows
description: Retrieves the list of supported resolutions for the specified codec.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_OUTPUT_RESOLUTION](ne-d3d12video-d3d12_feature_video.md). Retrieves the list of supported resolutions for the specified codec.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which the supported resolutions are being queried.

### -field ResolutionRatiosCount

The number of resolution ratios to retrieve. This number must match the number in the [D3D12_FEATURE_DATA_VIDEO_ENCODER_OUTPUT_RESOLUTION_RATIOS_COUNT.ResolutionRatiosCount](ns-d3d12video-d3d12_feature_data_video_encoder_output_resolution_ratios_count.md) field returned from a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with **D3D12_FEATURE_VIDEO_ENCODER_OUTPUT_RESOLUTION_RATIOS_COUNT** specified as the feature.

### -field IsSupported

Receives a boolean indicating if the query inputs are supported.

### -field MinResolutionSupported

Receives the minimum resolution supported for the specified codec.

### -field MaxResolutionSupported

Receives the maximum resolution supported for the specified codec.

### -field ResolutionWidthMultipleRequirement

A UINT specifying a number by which the resolution width component must be divisible.

### -field ResolutionHeightMultipleRequirement

A UINT specifying a number by which the resolution height component must be divisible.

### -field pResolutionRatios

Receives a list of [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_RATIO_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) representing the supported resolution ratios for the specified codec as irreducible fractions. The caller must allocate the memory for this array based on the **ResolutionRatiosCount** field, and assign it to the query struct the call to ID3D12VideoDevice::CheckFeatureSupport.

## -remarks

## -see-also

