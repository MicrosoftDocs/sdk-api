---
UID: NF:d3d12video.ID3D12VideoDevice.CreateVideoDecoderHeap
title: ID3D12VideoDevice::CreateVideoDecoderHeap
description: Allocates a video decoder heap.
helpviewer_keywords: ["ID3D12VideoDevice::CreateVideoDecoderHeap","CreateVideoDecoderHeap","ID3D12VideoDevice.CreateVideoDecoderHeap","ID3D12VideoDevice::CreateVideoDecoderHeap","ID3D12VideoDevice.CreateVideoDecoderHeap"]
tech.root: mf
ms.assetid: 70b73a82-bbd2-490f-976a-ac7e4d23827c
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDevice::CreateVideoDecoderHeap, CreateVideoDecoderHeap, ID3D12VideoDevice.CreateVideoDecoderHeap, ID3D12VideoDevice::CreateVideoDecoderHeap, ID3D12VideoDevice.CreateVideoDecoderHeap
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
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - ID3D12VideoDevice::CreateVideoDecoderHeap
 - d3d12video/ID3D12VideoDevice::CreateVideoDecoderHeap
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice::CreateVideoDecoderHeap
---

# ID3D12VideoDevice::CreateVideoDecoderHeap


## -description

Allocates a video decoder heap that contains the resolution-dependent driver resources and state.

## -parameters

### -param pVideoDecoderHeapDesc

A pointer to a [D3D12\_VIDEO\_DECODER\_HEAP\_DESC](ns-d3d12video-d3d12_video_decoder_heap_desc.md) describing the decoding configuration.

### -param riid

The globally unique identifier (GUID) for the decode video state interface.

### -param ppVideoDecoderHeap

A pointer to a memory block that receives a pointer to the [ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md) interface.

## -returns

This method returns an HRESULT.

## -remarks

## -see-also

