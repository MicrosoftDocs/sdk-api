---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
ms.date: 04/07/2026
targetos: Windows
description: Provides data for calls to ID3D12VideoDevice::CheckFeatureSupport when the feature specified is D3D12_FEATURE_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
req.umdf-ver: 
req.unicode-ansi: 
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS](ne-d3d12video-d3d12_feature_video.md). Queries driver support for lower resolution two pass frame analysis at a given downscale factor and encode configuration.

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field Codec

Input parameter. A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the codec.

### -field Profile

Input parameter. A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the profile.

### -field Level

Input parameter. A [D3D12_VIDEO_ENCODER_LEVEL_SETTING](ns-d3d12video-d3d12_video_encoder_level_setting.md) specifying the level.

### -field InputFormat

Input parameter. A DXGI_FORMAT specifying the input format.

### -field InputResolution

Input parameter. A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) specifying the input resolution.

### -field CodecConfiguration

Input parameter. A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_codec_configuration.md) specifying the codec configuration.

### -field SubregionFrameEncoding

Input parameter. A [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md) specifying the subregion frame encoding mode.

### -field SubregionFrameEncodingData

Input parameter. A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA](ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data.md) specifying the subregion frame encoding data.

### -field QPMap

Input parameter. A D3D12_VIDEO_ENCODER_QPMAP_CONFIGURATION specifying the QP map configuration.

### -field DirtyRegions

Input parameter. A D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION specifying the dirty regions configuration.

### -field MotionSearch

Input parameter. A D3D12_VIDEO_ENCODER_MOTION_SEARCH_CONFIGURATION specifying the motion search configuration.

### -field Pow2DownscaleFactor

Input parameter. Indicates the downscaling ratio to be used for the two pass downscaled texture passed to the driver. The full resolution input dimensions must be exactly divisible by 2^*Pow2DownscaleFactor*. The drivers must also enforce this by reporting no support where the division is not exact.

### -field SupportFlags

Output parameter. A bitwise or combination of [D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_rate_control_frame_analysis_support_flags.md) values indicating support for the given input parameters.

## -remarks

## -see-also

[D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_rate_control_frame_analysis_support_flags.md)
