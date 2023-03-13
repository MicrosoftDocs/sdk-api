---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL
ms.date: 06/15/2021
targetos: Windows
description: Represents a video encoder rate control configuration.
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
req.typenames: D3D12_VIDEO_ENCODER_RATE_CONTROL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL
dev_langs:
 - c++
---

## -description

Represents a video encoder rate control configuration.

## -struct-fields

### -field Mode

A value from the [D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE](ne-d3d12video-d3d12_video_encoder_rate_control_mode.md) enumeration specifying the rate control mode.

### -field Flags

A bitwise OR combination of values from the [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAGS](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) enumeration.

### -field ConfigParams

A [D3D12_VIDEO_ENCODER_RATE_CONTROL_CONFIGURATION_PARAMS](ns-d3d12video-d3d12_video_encoder_rate_control_configuration_params.md) structure representing rate control configuration parameters corresponding to the specified *Mode*. Note that for absolute QP matrix mode, the configuration arguments are provided per EncodeFrame basis.

If the selected rate control mode is **D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_ABSOLUTE_QP_MAP**, the QP values in *pRateControlQPMap* are treated as absolute QP values.

For the other rate control modes,  the QP values in *pRateControlQPMap* are interpreted as a delta QP map to be used for the current frame encode operation. The values provided in the map are incremented/decremented on top of the QP values decided by the rate control algorithm or the baseline QP constant set in CQP mode.


### -field TargetFrameRate

A [DXGI_RATIONAL](/windows/win32/api/dxgicommon/ns-dxgicommon-dxgi_rational) specifying the target frame rate for the encoded stream. This value is a hint for the rate control budgeting algorithm.

## -remarks

## -see-also

