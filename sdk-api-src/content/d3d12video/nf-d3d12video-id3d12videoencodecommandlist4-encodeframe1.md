---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList4.EncodeFrame1
tech.root: mf
title: ID3D12VideoEncodeCommandList4::EncodeFrame1
ms.date: 04/07/2026
targetos: Windows
description: Encodes a bitstream, with support for subregion notification.
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
 - ID3D12VideoEncodeCommandList4::EncodeFrame1
f1_keywords:
 - ID3D12VideoEncodeCommandList4::EncodeFrame1
 - d3d12video/ID3D12VideoEncodeCommandList4::EncodeFrame1
dev_langs:
 - c++
helpviewer_keywords:
 - EncodeFrame1
---

## -description

Encodes a bitstream, with support for subregion notification.

## -parameters

### -param pEncoder

A [ID3D12VideoEncoder](nn-d3d12video-id3d12videoencoder.md) representing the video encoder to be used for the encode operation.

### -param pHeap

A [ID3D12VideoEncoderHeap](nn-d3d12video-id3d12videoencoderheap.md) representing the video encoder heap to be used for this operation.

The encoder heap object allocation must not be released before any in-flight GPU commands that reference it finish execution.

### -param pInputArguments

A pointer to a [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments1.md) representing input arguments for the encode operation.

### -param pOutputArguments

A pointer to a [D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments1.md) representing output arguments for the encode operation.

## -remarks

This method extends [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) by accepting [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments1.md) for optional metadata support and [D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments1.md) for subregion notification support.

The video encoder and video encoder heap may be used to record commands from multiple command lists, but may only be associated with one command list at a time. The application is responsible for synchronizing single accesses to the video encoder and video encoder heap at a time.

## -see-also

[ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md)

