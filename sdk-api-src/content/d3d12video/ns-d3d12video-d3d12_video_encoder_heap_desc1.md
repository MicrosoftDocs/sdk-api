---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_HEAP_DESC1
tech.root: mf
title: D3D12_VIDEO_ENCODER_HEAP_DESC1
ms.date: 04/07/2026
targetos: Windows
description: Describes an ID3D12VideoEncoderHeap1, extending D3D12_VIDEO_ENCODER_HEAP_DESC with a downscale factor for frame analysis.
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
req.typenames: D3D12_VIDEO_ENCODER_HEAP_DESC1
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
 - D3D12_VIDEO_ENCODER_HEAP_DESC1
f1_keywords:
 - D3D12_VIDEO_ENCODER_HEAP_DESC1
 - d3d12video/D3D12_VIDEO_ENCODER_HEAP_DESC1
dev_langs:
 - c++
---

## -description

Describes an [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md). Extends [D3D12_VIDEO_ENCODER_HEAP_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md) with a power-of-two downscale factor for lower resolution frame analysis.

## -struct-fields

### -field NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Flags

A bitwise or combination of values from the [D3D12_VIDEO_ENCODER_HEAP_FLAGS](ne-d3d12video-d3d12_video_encoder_heap_flags.md) enumeration specifying encoder heap creation options.

### -field EncodeCodec

A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the codec of the associated encoder object.

### -field EncodeProfile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the profile for the selected codec in the associated encoder object.

### -field EncodeLevel

A [D3D12_VIDEO_ENCODER_LEVEL_SETTING](ns-d3d12video-d3d12_video_encoder_level_setting.md) specifying the level for the selected codec in the associated encoder object.

### -field ResolutionsListCount

The count of resolutions requested to be supported present in the *pResolutionList* field.

### -field pResolutionList

Pointer to an array of [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) specifying the list of resolutions requested to be supported.

### -field Pow2DownscaleFactor

When [D3D12_VIDEO_ENCODER_HEAP_FLAG_ALLOW_RATE_CONTROL_FRAME_ANALYSIS](ne-d3d12video-d3d12_video_encoder_heap_flags.md) is set, indicates to the driver the downscaling factor for the 1st pass. The downscaled dimensions are calculated as InputWidth / 2^*Pow2DownscaleFactor* and InputHeight / 2^*Pow2DownscaleFactor*. When *Pow2DownscaleFactor* is 0 and the flag is set, the 1st pass is performed at full resolution.

## -remarks

If [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RESOLUTION_RECONFIGURATION_AVAILABLE](ne-d3d12video-d3d12_video_encoder_support_flags.md) is supported, *Pow2DownscaleFactor* applies to all possible resolutions that can be dynamically switched between or used with this [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md), listed in *pResolutionList*. When dynamically switching between resolutions, the 1st pass lower resolution is also adjusted accordingly.

## -see-also

[D3D12_VIDEO_ENCODER_HEAP_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md)

[ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md)
