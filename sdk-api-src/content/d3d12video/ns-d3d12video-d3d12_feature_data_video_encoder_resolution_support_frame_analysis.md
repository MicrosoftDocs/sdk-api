---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
ms.date: 04/07/2026
targetos: Windows
description: Defines the reported support for frame analysis per resolution.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_FRAME_ANALYSIS
dev_langs:
 - c++
---

## -description

Defines the reported support for frame analysis as output for D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1.

## -struct-fields

### -field SupportFlags

Output parameter. A bitwise or combination of [D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_rate_control_frame_analysis_support_flags.md) values indicating the supported frame analysis capabilities for this resolution.

## -remarks

Only reported when D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2.FrameAnalysis.Enabled is TRUE and the driver supports it. Zeroed memory otherwise.

## -see-also

[D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_rate_control_frame_analysis_support_flags.md)
