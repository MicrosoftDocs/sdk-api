---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC
ms.date: 06/29/2021
targetos: Windows
description: Specifies the type of an HEVC video frame.
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
 - D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC
dev_langs:
 - c++
---

## -description

Specifies the type of an HEVC video frame.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_I_FRAME

I-Frame. Completely intra-coded frame.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_P_FRAME

P-Frame. Allows references to past frames.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_B_FRAME

B-Frame. Allows references to both past and future (in display order) frames.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_IDR_FRAME

Instantaneous decode refresh frame. A special type of I-frame where no frame after it can reference any frame before it.

## -remarks

The following table lists the expected HEVC header frame type for each HEVC frame type value.

| Syntax element | Expected default value |
|---------------|---------------------------|
| D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_I_FRAME	| nal_unit_type = CRA_NUT |
| D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_P_FRAME	| nal_unit_type = TRAIL_R |
| D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_B_FRAME	| nal_unit_type = TRAIL_R |
| D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_IDR_FRAME	| nal_unit_type = IDR_W_RADL |


If [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_P_FRAMES_IMPLEMENTED_AS_LOW_DELAY_B_FRAMES](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc_flags.md) is set, it informs the caller that when encoding frames with type **D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_P_FRAME**, they will be written as low delay B-Frames in the compressed bitstream. If bit is not set, it informs the caller P frames will be written in the compressed bitstream. Note that When operating under this mode, is the caller's responsibility to code the correct frame type in AUD_NUT and other parts of the HEVC bitstream, taking into account that P frames will be treated as generalized B frames with only references to past frames in POC order.

## -see-also

