---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_HEAP_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_HEAP_FLAGS
ms.date: 06/08/2021
targetos: Windows
description: Specifies heap options for video encoding.
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
 - D3D12_VIDEO_ENCODER_HEAP_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_HEAP_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_HEAP_FLAGS
dev_langs:
 - c++
---

## -description

Specifies heap options for video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_HEAP_FLAG_NONE

No flags.

### -field D3D12_VIDEO_ENCODER_HEAP_FLAG_ALLOW_DIRTY_REGIONS

Indicates that the encoder heap supports dirty regions. Required when using [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_ENABLE_DIRTY_REGIONS_INPUT](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md).

### -field D3D12_VIDEO_ENCODER_HEAP_FLAG_ALLOW_RATE_CONTROL_FRAME_ANALYSIS

Indicates to the driver that two pass will be used with the associated [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md). The driver uses this flag to allocate and initialize the internal state required for storing two pass context in this object.

## -remarks

## -see-also

