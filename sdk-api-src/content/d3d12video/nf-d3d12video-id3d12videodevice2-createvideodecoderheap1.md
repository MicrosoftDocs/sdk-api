---
UID: NF:d3d12video.ID3D12VideoDevice2.CreateVideoDecoderHeap1
title: ID3D12VideoDevice2::CreateVideoDecoderHeap1
description: Allocates a video decoder heap that contains the resolution-dependent driver resources and state, with support for protected resources.
tech.root: mf
ms.date: 8/19/2019
ms.keywords: ID3D12VideoDevice2::CreateVideoDecoderHeap1
targetos: Windows
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D12VideoDevice2::CreateVideoDecoderHeap1
 - d3d12video/ID3D12VideoDevice2::CreateVideoDecoderHeap1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoDevice2::CreateVideoDecoderHeap1
---

## -description

Allocates a video decoder heap that contains the resolution-dependent driver resources and state, with support for protected resources.

## -parameters

### -param pVideoDecoderHeapDesc

A pointer to a [D3D12\_VIDEO\_DECODER\_HEAP\_DESC](ns-d3d12video-d3d12_video_decoder_heap_desc.md) describing the decoding configuration.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the decode video state interface.

### -param ppVideoDecoderHeap

A pointer to a memory block that receives a pointer to the [ID3D12VideoDecoderHeap1](nn-d3d12video-id3d12videodecoderheap1.md) interface.

## -returns

This method returns an HRESULT.

## -remarks

## -see-also
