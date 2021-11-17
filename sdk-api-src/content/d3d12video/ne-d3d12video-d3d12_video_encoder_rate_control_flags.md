---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS
ms.date: 06/15/2021
targetos: Windows
description: Specifies flags for a 3D12_VIDEO_ENCODER_RATE_CONTROL structure. 
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
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS
dev_langs:
 - c++
---

## -description

Specifies flags for a [D3D12_VIDEO_ENCODER_RATE_CONTROL](ns-d3d12video-d3d12_video_encoder_rate_control.md) structure. 

## -enum-fields

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_DELTA_QP

If the selected rate control is [D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_ABSOLUTE_QP_MAP](ne-d3d12video-d3d12_video_encoder_rate_control_mode.md), this flag has no effect since the QP values in **D3D12_VIDEO_ENCODER_RATE_CONTROL.pRateControlQPMap** field are used as absolute QP values.

For the other rate control modes, this flag enables the usage of **D3D12_VIDEO_ENCODER_RATE_CONTROL.pRateControlQPMap** to be interpreted as a delta QP map to be used for the current frame encode operation. The values provided in the map are incremented/decremented on top of the QP values decided by the rate control algorithm or the baseline QP constant set in CQP mode.

**Note** Using delta QP adjustment along with some active rate control modes may violate bitrate constraints as it's explicitly altering the QP values that were selected by rate control budgeting algorithm.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_FRAME_ANALYSIS

If [D3D12_VIDEO_ENCODER_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_support_flags.md) is supported, Enables the rate control algorithm to optimize bitrate usage by selecting QP values based on statistics collected by doing frame analysis on a first pass.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_QP_RANGE

The MinQp/MaxQP values are used as a range for the rate control algorithm.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_INITIAL_QP

The InitialQP values are used as a range for the rate control algorithm.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_MAX_FRAME_SIZE

When [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RATE_CONTROL_MAX_FRAME_SIZE](ne-d3d12video-d3d12_video_encoder_support_flags.md) is supported, the rate control algorithm will limit the maximum size per frame to the specified parameter in the rate control configuration. 

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_VBV_SIZES

Enables the usage of VBVCapacity and InitialVBVFullness.

## -remarks

## -see-also

