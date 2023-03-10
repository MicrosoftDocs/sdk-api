---
UID: NS:d3d12video.D3D12_VIDEO_DECODER_DESC
title: D3D12_VIDEO_DECODER_DESC
description: Describes a ID3D12VideoDecoder.
helpviewer_keywords: ["D3D12_VIDEO_DECODER_DESC","D3D12_VIDEO_DECODER_DESC",""]
tech.root: mf
ms.assetid: 0e50bf0f-f160-4214-98da-80b4badb4989
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODER_DESC, D3D12_VIDEO_DECODER_DESC,
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
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODER_DESC
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODER_DESC
 - d3d12video/D3D12_VIDEO_DECODER_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODER_DESC
---

# D3D12_VIDEO_DECODER_DESC structure


## -description

Describes a [ID3D12VideoDecoder](nn-d3d12video-id3d12videodecoder.md). Pass this structure into [ID3D12VideoDevice::CreateVideoDecoder](nf-d3d12video-id3d12videodevice-createvideodecoder.md) to create an instance of **ID3D12VideoDecoder**.

## -struct-fields

### -field NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Configuration

A [D3D12_VIDEO_DECODE_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration.md) structure specifying the configuration of the video decoder.

## -remarks

## -see-also

