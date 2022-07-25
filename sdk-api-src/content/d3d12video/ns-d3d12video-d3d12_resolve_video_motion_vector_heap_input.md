---
UID: NS:d3d12video.D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
title: D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
ms.date: 11/4/2019
targetos: Windows
description: Provides input data for calls to ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap.
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
req.typenames: D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
f1_keywords:
 - D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
 - d3d12video/D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT
dev_langs:
 - c++
---

## -description

Provides input data for calls to [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap.md).

## -struct-fields

### -field pMotionVectorHeap

The [ID3D12VideoMotionVectorHeap](nn-d3d12video-id3d12videomotionvectorheap.md) containing the hardware-dependent data layout of the motion search.

### -field PixelWidth

The pixel width of the texture that the motion estimation operation was performed on. The motion estimator heap may be allocated to support a size range, this parameter informs the size of the last motion estimation operation.

### -field PixelHeight

The pixel height of the texture that the motion estimation operation was performed on. The motion estimator heap may be allocated to support a size range, this parameter informs the size of the last motion estimation operation.

## -remarks

## -see-also

