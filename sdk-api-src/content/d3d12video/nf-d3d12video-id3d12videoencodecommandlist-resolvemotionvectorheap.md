---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.ResolveMotionVectorHeap
title: ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap
ms.date: 11/4/2019
targetos: Windows
description: Translates the motion vector output of the EstimateMotion method from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap
f1_keywords:
 - ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap
 - d3d12video/ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap
dev_langs:
 - c++
---

## -description

Translates the motion vector output of the [EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md) method from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.

## -parameters

### -param pOutputArguments

A [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output.md) structure containing the translated motion vectors.

### -param pInputArguments

A [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input.md) structure containing the  motion vectors to translate.

## -remarks

## -see-also

