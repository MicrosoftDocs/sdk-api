---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
ms.date: 06/15/2021
targetos: Windows
description: Represents video encoder rate control structure definitions for a D3D12_VIDEO_ENCODER_RATE_CONTROL structure.
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
req.typenames: D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS
dev_langs:
 - c++
---

## -description

Represents video encoder rate control structure definitions for a [D3D12_VIDEO_ENCODER_RATE_CONTROL](ns-d3d12video-d3d12_video_encoder_rate_control.md) structure.

## -struct-fields

### -field DataSize

The data size of the provided rate control structure.

### -field pConfiguration_CQP

A [D3D12_VIDEO_ENCODER_RATE_CONTROL_CQP](ns-d3d12video-d3d12_video_encoder_rate_control_cqp.md) structure representing the rate control structure definition for constant quantization parameter mode.

### -field pConfiguration_CBR

A [D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR](ns-d3d12video-d3d12_video_encoder_rate_control_cbr.md) structure representing the rate control structure definition for constant bitrate mode.

### -field pConfiguration_VBR

A [D3D12_VIDEO_ENCODER_RATE_CONTROL_VBR](ns-d3d12video-d3d12_video_encoder_rate_control_cqp.md) structure representing the rate control structure definition for variable bitrate mode.

### -field pConfiguration_QVBR

A [D3D12_VIDEO_ENCODER_RATE_CONTROL_QVBR](ns-d3d12video-d3d12_video_encoder_rate_control_vbr.md) structure representing the rate control structure definition for constant quality target with constrained bitrate mode.

## -remarks

## -see-also

