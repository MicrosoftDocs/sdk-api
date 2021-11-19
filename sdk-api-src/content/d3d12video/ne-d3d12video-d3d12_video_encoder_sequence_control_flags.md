---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAGS
ms.date: 06/30/2021
targetos: Windows
description: Specifies flags for video encoder sequence control properties.
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
 - D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAGS
dev_langs:
 - c++
---

## -description

Specifies flags for video encoder sequence control properties.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_RESOLUTION_CHANGE

Indicates a change in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.PictureTargetResolution](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md).

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_RATE_CONTROL_CHANGE

Indicates a change in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.RateControl]((ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md).

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_SUBREGION_LAYOUT_CHANGE

Indicates a change in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.SelectedLayoutMode](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md) or [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.pFrameSubregionsLayoutData](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md).

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_REQUEST_INTRA_REFRESH

Starts an intra-refresh session starting at this frame using the configuration in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.IntraRefreshConfig](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md).

### -field D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_GOP_SEQUENCE_CHANGE

Indicates a change in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.CodecGOPSequence](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md).

## -remarks

Note that depending on the codec, a request for reconfiguration might need to insert an IDR in the bitstream and new SPS headers.

## -see-also

