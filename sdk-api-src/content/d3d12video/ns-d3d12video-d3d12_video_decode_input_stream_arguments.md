---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
title: D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
description: Specifies the parameters for the input stream for a video decode operation.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS","D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS",""]
tech.root: mf
ms.assetid: 6eaa5bd2-2381-494c-b081-e1d72fe175f3
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS, D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS,
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
req.typenames: D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
 - d3d12video/D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS
---

# D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS structure


## -description

Specifies the parameters for the input stream for a video decode operation.

## -struct-fields

### -field NumFrameArguments

The count of frame parameters provided in the *FrameArguments* field. The maximum number of frame arguments is 10.

### -field FrameArguments

An array of [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](ns-d3d12video-d3d12_video_decode_frame_argument.md) structures containing the parameters to decode a frame.

### -field ReferenceFrames

A [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](ns-d3d12video-d3d12_video_decode_reference_frames.md) structure containing the reference frames needed to decode a frame.

### -field CompressedBitstream

A [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_decode_compressed_bitstream.md) structure representing the compressed bitstream in a single continuous buffer.

### -field pHeap

 
An [ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md) representing a pointer to the heap for the current decode resolution.

## -remarks

## -see-also

