---
UID: NF:d3d12video.ID3D12VideoDevice1.CreateVideoMotionVectorHeap
title: ID3D12VideoDevice1::CreateVideoMotionVectorHeap
description: Allocates heap that contains motion vectors for video motion estimation.
tech.root: mf
ms.date: 4/26/2019
ms.keywords: ID3D12VideoDevice1::CreateVideoMotionVectorHeap
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D12VideoDevice1::CreateVideoMotionVectorHeap
 - d3d12video/ID3D12VideoDevice1::CreateVideoMotionVectorHeap
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice1::CreateVideoMotionVectorHeap
---

## -description

Allocates heap that contains motion vectors for video motion estimation.

## -parameters

### -param pDesc

A pointer to a [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](ns-d3d12video-d3d12_video_motion_vector_heap_desc.md) describing the format of the heap. This structure contains both input and output fields.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the **ID3D12VideoMotionVectorHeap** interface.

### -param ppVideoMotionVectorHeap

A pointer to a memory block that receives a pointer to the **ID3D12VideoMotionVectorHeap** interface.

## -returns

This method returns HRESULT.

## -remarks

## -see-also
