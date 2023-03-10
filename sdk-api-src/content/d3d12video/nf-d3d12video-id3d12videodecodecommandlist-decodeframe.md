---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.DecodeFrame
title: ID3D12VideoDecodeCommandList::DecodeFrame
description: Records a decode frame operation to the command list.
helpviewer_keywords: ["ID3D12VideoDecodeCommandList::DecodeFrame","DecodeFrame","ID3D12VideoDecodeCommandList.DecodeFrame","ID3D12VideoDecodeCommandList::DecodeFrame","ID3D12VideoDecodeCommandList.DecodeFrame"]
tech.root: mf
ms.assetid: c3d8c964-b411-440a-bc79-b3abbf32b40f
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDecodeCommandList::DecodeFrame, DecodeFrame, ID3D12VideoDecodeCommandList.DecodeFrame, ID3D12VideoDecodeCommandList::DecodeFrame, ID3D12VideoDecodeCommandList.DecodeFrame
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
 - ID3D12VideoDecodeCommandList::DecodeFrame
 - d3d12video/ID3D12VideoDecodeCommandList::DecodeFrame
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::DecodeFrame
---

# ID3D12VideoDecodeCommandList::DecodeFrame


## -description

Records a decode frame operation to the command list.  Inputs, outputs, and parameters for the decode are specified as arguments to this method.

## -parameters

### -param pDecoder

A pointer to an [ID3D12VideoDecoder](nn-d3d12video-id3d12videodecoder.md) interface representing a decoder instance.

### -param pOutputArguments

A [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_decode_output_stream_arguments.md) structure specifying the output surface and output arguments.

### -param pInputArguments

A [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_decode_input_stream_arguments.md) structure specifying the input bitstream, reference frames, and other input parameters.

## -remarks

The [ID3D12VideoDecodeCommandList1::DecodeFrame1](nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1.md) method provides the same functionality as this method, but adds support for decode histograms.

## -see-also

