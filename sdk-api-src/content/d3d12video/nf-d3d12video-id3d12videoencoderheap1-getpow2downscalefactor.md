---
UID: NF:d3d12video.ID3D12VideoEncoderHeap1.GetPow2DownscaleFactor
tech.root: mf
title: ID3D12VideoEncoderHeap1::GetPow2DownscaleFactor
ms.date: 04/07/2026
targetos: Windows
description: Gets the power-of-two downscale factor for the video encoder heap.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID3D12VideoEncoderHeap1::GetPow2DownscaleFactor
f1_keywords:
 - ID3D12VideoEncoderHeap1::GetPow2DownscaleFactor
 - d3d12video/ID3D12VideoEncoderHeap1::GetPow2DownscaleFactor
dev_langs:
 - c++
---

## -description

Gets the power-of-two downscale factor for the video encoder heap.

## -returns

When the [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md) object was created with [D3D12_VIDEO_ENCODER_HEAP_FLAG_ALLOW_RATE_CONTROL_FRAME_ANALYSIS](ne-d3d12video-d3d12_video_encoder_heap_flags.md), returns the value of *Pow2DownscaleFactor* used at creation. Zero otherwise.

## -remarks

## -see-also

[ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md)

[D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md)
