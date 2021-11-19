---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_HEAP_DESC
tech.root: mf
title: D3D12_VIDEO_ENCODER_HEAP_DESC
ms.date: 06/08/2021
targetos: Windows
description: Describes a ID3D12VideoEncoderHeap.
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
req.typenames: D3D12_VIDEO_ENCODER_HEAP_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_HEAP_DESC
f1_keywords:
 - D3D12_VIDEO_ENCODER_HEAP_DESC
 - d3d12video/D3D12_VIDEO_ENCODER_HEAP_DESC
dev_langs:
 - c++
---

## -description

Describes a [ID3D12VideoEncoderHeap](nn-d3d12video-id3d12videoencoderheap.md). Pass this structure into [ID3D12VideoDevice3::CreateVideoEncoderHeap](nf-d3d12video-id3d12videodevice3-createvideoencoderheap.md) to create an instance of **ID3D12VideoEncoderHeap**.

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

## -remarks

If support for resolution dynamic reconfiguration is not supported, specify only one resolution in *pResolutionList*, denoting the desired target resolution.

## -see-also

[ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md)

[ID3D12VideoDevice3::CreateVideoEncoderHeap](nf-d3d12video-id3d12videodevice3-createvideoencoderheap.md)
