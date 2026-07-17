---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
ms.date: 04/07/2026
targetos: Windows
description: Describes the frame analysis configuration for a video encoder support query.
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
req.typenames: D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
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
 - D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_ANALYSIS_CONFIGURATION
dev_langs:
 - c++
---

## -description

Describes the frame analysis configuration for a video encoder support query.

## -struct-fields

### -field Enabled

A boolean value indicating whether frame analysis is enabled for this support query.

### -field Pow2DownscaleFactor

The power-of-two downscale factor for the frame analysis pass. For example, a value of 1 means the 1st pass dimensions are half the full resolution, and a value of 2 means the 1st pass dimensions are a quarter of the full resolution. A value of 0 indicates full resolution frame analysis.

## -remarks

## -see-also

[D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS](ns-d3d12video-d3d12_feature_data_video_encoder_rate_control_frame_analysis.md)
