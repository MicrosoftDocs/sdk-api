---
UID: NF:d3d12video.ID3D12VideoDevice2.CreateVideoDecoder1
title: ID3D12VideoDevice2::CreateVideoDecoder1
description: Creates a video decoder instance that contains the resolution-independent driver resources and state, with support for protected resources.
tech.root: mf
ms.date: 8/19/2019
ms.keywords: ID3D12VideoDevice2::CreateVideoDecoder1
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
 - ID3D12VideoDevice2::CreateVideoDecoder1
 - d3d12video/ID3D12VideoDevice2::CreateVideoDecoder1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoDevice2::CreateVideoDecoder1
---

## -description

Creates a video decoder instance that contains the resolution-independent driver resources and state, with support for protected resources.

## -parameters

### -param pDesc

A pointer to a [D3D12\_VIDEO\_DECODER\_DESC](ns-d3d12video-d3d12_video_decoder_desc.md) structure describing the decode profile and bitstream encryption for the decoder.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the decode video state interface.

### -param ppVideoDecoder

A pointer to a memory block that receives a pointer to the [ID3D12VideoDecoder1](nn-d3d12video-id3d12videodecoder1.md) interface.

## -returns

This method returns HRESULT.

## -remarks

Decoding a new stream requires instantiating a new decoder object.

## -see-also
