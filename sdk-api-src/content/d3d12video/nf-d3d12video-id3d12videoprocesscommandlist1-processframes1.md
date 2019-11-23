---
UID: NF:d3d12video.ID3D12VideoProcessCommandList1.ProcessFrames1
title: ID3D12VideoProcessCommandList1::ProcessFrames1

description: Records a video processing operation to the command list, operating on one or more input samples and writing the result to an output surface.
tech.root: mf
ms.assetid: a0310ab9-bf11-4a40-a463-6ad6cf7fd3eb

ms.date: 05/28/2019
ms.topic: method
f1_keywords:
 - ID3D12VideoProcessCommandList1::ProcessFrames1
dev_langs:
 - c++
ms.keywords: ID3D12VideoProcessCommandList1::ProcessFrames1, ProcessFrames1, ID3D12VideoProcessCommandList1.ProcessFrames1, ID3D12VideoProcessCommandList1::ProcessFrames1, ID3D12VideoProcessCommandList1.ProcessFrames1
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
 - ID3D12VideoProcessCommandList1::ProcessFrames1
targetos: Windows

---

# ID3D12VideoProcessCommandList1::ProcessFrames1


## -description

Records a video processing operation to the command list, operating on one or more input samples and writing the result to an output surface. This version of the method supports changing the [D3D12_VIDEO_FIELD_TYPE](ne-d3d12video-d3d12_video_field_type) for each call, unlike [ID3D12VideoProcessCommandList::ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes).

## -parameters

### -param pVideoProcessor

A pointer to an [ID3D12VideoProcessor](nn-d3d12video-id3d12videoprocessor) interface representing a video processor instance. 

### -param pOutputArguments

A [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_output_stream_arguments) structure specifying the output surface and output arguments.

### -param NumInputStreams

The count of input streams.

### -param pInputArguments

A pointer to an array of [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_process_input_stream_arguments1) structures specifying the input parameters.

## -returns
This method returns void.

## -remarks

## -see-also

