---
UID: NF:d3d12video.ID3D12VideoDevice3.CreateVideoEncoderHeap
tech.root: mf
title: ID3D12VideoDevice3::CreateVideoEncoderHeap
ms.date: 07/07/2021
targetos: Windows
description: Creates a new instance of ID3D12VideoEncoderHeap.
prerelease: false
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - ID3D12VideoDevice3::CreateVideoEncoderHeap
f1_keywords:
 - ID3D12VideoDevice3::CreateVideoEncoderHeap
 - d3d12video/ID3D12VideoDevice3::CreateVideoEncoderHeap
dev_langs:
 - c++
---

## -description

Creates a new instance of [ID3D12VideoEncoderHeap](nn-d3d12video-id3d12videoencoderheap.md).

## -parameters

### -param pDesc

A [D3D12_VIDEO_ENCODER_HEAP_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md) representing the configuration parameters for the video encoder heap.

### -param riid

The globally unique identifier (GUID) for the video encoder heap interface. Expected value: IID_ID3D12VideoEncoderHeap.

### -param ppVideoEncoderHeap

A pointer to a memory block that receives a pointer to the video encoder heap interface.

## -returns

## -remarks

## -see-also

