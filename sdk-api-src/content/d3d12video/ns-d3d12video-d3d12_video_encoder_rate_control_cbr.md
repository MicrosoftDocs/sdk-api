---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
ms.date: 06/15/2021
targetos: Windows
description: Represents a rate control structure definition for constant bitrate mode.
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
req.typenames: D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_CBR
dev_langs:
 - c++
---

## -description

Represents a rate control structure definition for constant bitrate mode.

## -struct-fields

### -field InitialQP

When [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_INITIAL_QP](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, allows the Initial QP to be used by the rate control algorithm.

### -field MinQP

When [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_QP_RANGE](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, limits QP range of the rate control algorithm.

### -field MaxQP

When [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_QP_RANGE](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, limits QP range of the rate control algorithm.

### -field MaxFrameBitSize

Maximum size in bits for each frame to be coded. When [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_MAX_FRAME_SIZE](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, limits each frame maximum size in the rate control algorithm.

### -field TargetBitRate

Specifies the constant bitrate to be used in bits/second.

### -field VBVCapacity

When [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RATE_CONTROL_VBV_SIZE_CONFIG_AVAILABLE](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, specifies the capacity in bits of the Video Buffer Verifier to be used in the rate control algorithm.

### -field InitialVBVFullness

When [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RATE_CONTROL_VBV_SIZE_CONFIG_AVAILABLE](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) is enabled, specifies the initial fullness in bits of the Video Buffer Verifier to be used in the rate control algorithm.

## -remarks



## -see-also

