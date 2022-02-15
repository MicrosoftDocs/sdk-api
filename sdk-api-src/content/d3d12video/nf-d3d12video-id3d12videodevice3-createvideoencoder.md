---
UID: NF:d3d12video.ID3D12VideoDevice3.CreateVideoEncoder
tech.root: mf
title: ID3D12VideoDevice3::CreateVideoEncoder
ms.date: 06/23/2021
targetos: Windows
description: Creates a new instance of ID3D12VideoEncoder.
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
 - ID3D12VideoDevice3::CreateVideoEncoder
f1_keywords:
 - ID3D12VideoDevice3::CreateVideoEncoder
 - d3d12video/ID3D12VideoDevice3::CreateVideoEncoder
dev_langs:
 - c++
---

## -description

Creates a new instance of [ID3D12VideoEncoder](nn-d3d12video-id3d12videoencoder.md).

## -parameters

### -param pDesc

A [D3D12_VIDEO_ENCODER_DESC](ns-d3d12video-d3d12_video_encoder_desc.md) representing the configuration parameters for the video encoder.

### -param riid

The globally unique identifier (GUID) for the video encoder interface. Expected value: IID_ID3D12VideoEncoder.

### -param ppVideoEncoder

A pointer to a memory block that receives a pointer to the video encoder interface.

## -returns

Returns S_OK on success.

## -remarks

## -see-also

