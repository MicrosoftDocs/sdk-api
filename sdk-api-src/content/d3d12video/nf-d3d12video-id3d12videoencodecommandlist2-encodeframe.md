---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList2.EncodeFrame
tech.root: mf
title: ID3D12VideoEncodeCommandList2::EncodeFrame
ms.date: 07/02/2021
targetos: Windows
description: Encodes a bitstream.
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
 - ID3D12VideoEncodeCommandList2::EncodeFrame
f1_keywords:
 - ID3D12VideoEncodeCommandList2::EncodeFrame
 - d3d12video/ID3D12VideoEncodeCommandList2::EncodeFrame
dev_langs:
 - c++
---

## -description

Encodes a bitstream.

## -parameters

### -param pEncoder

A [ID3D12VideoEncoder](nn-d3d12video-id3d12videoencoder.md) representing the video encoder to be used for the encode operation.

### -param pHeap

A [ID3D12VideoEncoderHeap](nn-d3d12video-id3d12videoencoderheap.md) representing the video encoder heap to be used for this operation.

The encoder heap object allocation must not be released before any in-flight GPU commands that references it finish execution. 

Note that the reconfigurations in recorded commands input arguments done within allowed bounds (e.g. different target resolutions in allowed lists of resolutions) can co-exist in-flight with the same encoder heap instance, providing the target resolution is supported by the given encoder heap.

In the current release, we only support one execution flow at a time using the same encoder or encoder heap instances. All commands against these objects must be recorded and submitted in a serialized order, i.e. from a single CPU thread or synchronizing multiple threads in such way that the commands are recorded in a serialized order.

The video encoder and video encoder heap may be used to record commands from multiple command lists, but may only be associated with one command list at a time. The application is responsible for synchronizing single accesses to the video encoder and video encoder heap at a time. The application must also record video encoding commands against the video encoder and video encoder heaps in the order that they are executed on the GPU.


### -param pInputArguments

A [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments.md) representing input arguments for the encode operation.

### -param pOutputArguments

A [D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments.md) representing output arguments for the encode operation.

## -remarks

## -see-also

