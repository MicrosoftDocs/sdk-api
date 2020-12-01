---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_REFERENCE_FRAMES
title: D3D12_VIDEO_DECODE_REFERENCE_FRAMES
description: Contains the list of reference frames for the current decode operation.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_REFERENCE_FRAMES","D3D12_VIDEO_DECODE_REFERENCE_FRAMES",""]
tech.root: mf
ms.assetid: 9b0151d7-aaeb-4f85-bd41-b68df916b9d0
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_REFERENCE_FRAMES, D3D12_VIDEO_DECODE_REFERENCE_FRAMES,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_REFERENCE_FRAMES
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_REFERENCE_FRAMES
 - d3d12video/D3D12_VIDEO_DECODE_REFERENCE_FRAMES
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_REFERENCE_FRAMES
---

# D3D12_VIDEO_DECODE_REFERENCE_FRAMES structure


## -description

Contains the list of reference frames for the current decode operation.  Either a texture array or an array of textures can be specified.

## -struct-fields

### -field NumTexture2Ds

The number of references specified in the *ppTexture2Ds* field.

### -field ppTexture2Ds

A list of reference textures. When specifying texture arrays, each entry will be point to the same resource. When specifying an array of textures, each entry will point to a separate resource.

### -field pSubresources

An array of subresource indices for the reference textures specified in *ppTexture2Ds*.  NULL indicates that subresource 0 should be assumed for each resource.

With texture arrays within a single resource, the subresource indices point to the array index of the first resource plane. With an array of textures in individual resources, the subresource index is typically zero.

The video device driver uses the "PicEntry" indices defined in the DXVA spec for the codec to dereference this array to find the subresource index to use with the corresponding resource. For example, in HEVC, the Driver uses [DXVA_PicEntry_HEVC::Index7Bits](/windows/win32/medfound/dxva-picentry-hevc) as an index for this array.

### -field ppHeaps

 
An array of [ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md) objects. This field is used with formats that support non-key frame resolution changes, allowing the caller to pass in the previous resolution's heap, relative to the reference it's being used for, in addition to the current resolution heap.

## -remarks

Reference textures may have limitations such as a requirement to allocate reference buffers as a texture array.  For information on the requirements for different decoder configurations, see [D3D12_VIDEO_DECODE_TIER](ne-d3d12video-d3d12_video_decode_tier.md).

## -see-also

