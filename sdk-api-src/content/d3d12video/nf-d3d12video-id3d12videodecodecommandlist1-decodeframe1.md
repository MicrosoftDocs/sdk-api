---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList1.DecodeFrame1
title: ID3D12VideoDecodeCommandList1::DecodeFrame1
author: windows-sdk-content
description: Records a decode frame operation to the command list.  Inputs, outputs, and parameters for the decode are specified as arguments to this method.
tech.root: mf
ms.assetid: 46d35b8a-ae2d-4df8-ad68-eaf840369cca
ms.author: windowssdkdev
ms.date: 05/28/2019
ms.topic: method
ms.keywords: ID3D12VideoDecodeCommandList1::DecodeFrame1, DecodeFrame1, ID3D12VideoDecodeCommandList1.DecodeFrame1, ID3D12VideoDecodeCommandList1::DecodeFrame1, ID3D12VideoDecodeCommandList1.DecodeFrame1
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
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList1::DecodeFrame1
product: Windows
targetos: Windows

---

# ID3D12VideoDecodeCommandList1::DecodeFrame1


## -description

Records a decode frame operation to the command list.  Inputs, outputs, and parameters for the decode are specified as arguments to this method. Takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure to support video decode histograms.

## -parameters

### -param pDecoder

A pointer to an [ID3D12VideoDecoder](nn-d3d12video-id3d12videodecoder) interface representing a decoder instance. 

### -param pOutputArguments

A [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure specifying the output surface and output arguments.

### -param pInputArguments

A [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_decode_input_stream_arguments) structure specifying the input bitstream, reference frames, and other input parameters.

## -returns

This method returns void.

## -remarks



## -see-also