---
UID: NS:d3d12video.D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
title: D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
ms.date: 11/4/2019
targetos: Windows
description: Receives output data from calls to ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
f1_keywords:
 - D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
 - d3d12video/D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT
dev_langs:
 - c++
---

## -description

Receives output data from calls to [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap.md).

## -struct-fields

### -field pMotionVectorTexture2D

An [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md) representing the output resource for resolved motion vectors. Motion vectors are resolved to [DXGI_FORMAT_R16G16_SINT](../dxgiformat/ne-dxgiformat-dxgi_format.md) 2D textures. The resolved data is a signed 16-byte integer with quarter PEL units with the X vector component stored in the R component and the Y vector component stored in the G component. Motion vectors are stored in a 2D layout that corresponds to the pixel layout of the original input textures.

### -field MotionVectorCoordinate

A [D3D12_RESOURCE_COORDINATE](ns-d3d12video-d3d12_resource_coordinate.md) structure specifying the output origin of the motion vectors. The remaining sub-region must be large enough to store all motion vectors per block specified by the input pixel with and pixel height and the specified [D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE](ne-d3d12video-d3d12_video_motion_estimator_search_block_size.md).

## -remarks

## -see-also