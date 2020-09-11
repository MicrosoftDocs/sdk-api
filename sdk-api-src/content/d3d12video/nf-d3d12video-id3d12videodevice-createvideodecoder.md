---
UID: NF:d3d12video.ID3D12VideoDevice.CreateVideoDecoder
title: ID3D12VideoDevice::CreateVideoDecoder
description: Creates a video decoder instance.
helpviewer_keywords: ["ID3D12VideoDevice::CreateVideoDecoder","CreateVideoDecoder","ID3D12VideoDevice.CreateVideoDecoder","ID3D12VideoDevice::CreateVideoDecoder","ID3D12VideoDevice.CreateVideoDecoder"]
tech.root: mf
ms.assetid: 13e547db-b7b9-4664-9859-ba76d7eaac10
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDevice::CreateVideoDecoder, CreateVideoDecoder, ID3D12VideoDevice.CreateVideoDecoder, ID3D12VideoDevice::CreateVideoDecoder, ID3D12VideoDevice.CreateVideoDecoder
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
 - ID3D12VideoDevice::CreateVideoDecoder
 - d3d12video/ID3D12VideoDevice::CreateVideoDecoder
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice::CreateVideoDecoder
---

# ID3D12VideoDevice::CreateVideoDecoder


## -description

Creates a video decoder instance that contains the resolution-independent driver resources and state.

## -parameters

### -param pDesc

A pointer to a [D3D12\_VIDEO\_DECODER\_DESC](ns-d3d12video-d3d12_video_decoder_desc.md) structure describing the decode profile and bitstream encryption for the decoder.

### -param riid

The globally unique identifier (GUID) for the decode video state interface.

### -param ppVideoDecoder

A pointer to a memory block that receives a pointer to the [ID3D12VideoDecoder](nn-d3d12video-id3d12videodecoder.md) interface.

## -returns

This method returns HRESULT.

## -remarks

Decoding a new stream requires instantiating a new decoder object.

## -see-also

