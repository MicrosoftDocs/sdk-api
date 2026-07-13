---
UID: NF:d3d12video.ID3D12VideoProcessCommandList.ProcessFrames
title: ID3D12VideoProcessCommandList::ProcessFrames
description: Records a video processing operation to the command list, operating on one or more input samples and writing the result to an output surface. (ID3D12VideoProcessCommandList::ProcessFrames)
helpviewer_keywords: ["ID3D12VideoProcessCommandList::ProcessFrames","ProcessFrames","ID3D12VideoProcessCommandList.ProcessFrames","ID3D12VideoProcessCommandList::ProcessFrames","ID3D12VideoProcessCommandList.ProcessFrames"]
tech.root: mf
ms.assetid: 7f94fe17-318e-49cd-8041-71ca34030572
ms.date: 05/28/2019
ms.keywords: ID3D12VideoProcessCommandList::ProcessFrames, ProcessFrames, ID3D12VideoProcessCommandList.ProcessFrames, ID3D12VideoProcessCommandList::ProcessFrames, ID3D12VideoProcessCommandList.ProcessFrames
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
 - ID3D12VideoProcessCommandList::ProcessFrames
 - d3d12video/ID3D12VideoProcessCommandList::ProcessFrames
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoProcessCommandList::ProcessFrames
---

# ID3D12VideoProcessCommandList::ProcessFrames


## -description

Records a video processing operation to the command list, operating on one or more input samples and writing the result to an output surface.

> [!NOTE] 
> This version of the method does not allow you to change the [D3D12_VIDEO_FIELD_TYPE](ne-d3d12video-d3d12_video_field_type.md) without recreating the interface. It is recommended that you use [ID3D12VideoProcessCommandList::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md) instead, which allows you to change the field type with each call.

## -parameters

### -param pVideoProcessor

A pointer to an [ID3D12VideoProcessor](nn-d3d12video-id3d12videoprocessor.md) interface representing a video processor instance.

### -param pOutputArguments

A [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_output_stream_arguments.md) structure specifying the output surface and output arguments.

### -param NumInputStreams

The count of input streams.

### -param pInputArguments

A pointer to an array of [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_input_stream_arguments.md) structures specifying the input parameters.

## -remarks

This version of the method does not allow you to change the [D3D12_VIDEO_FIELD_TYPE](ne-d3d12video-d3d12_video_field_type.md). When dealing with mixed content, use [ID3D12VideoProcessCommandList::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md) instead, which allows you to specify a field type with each call.

## -see-also

[ID3D12VideoProcessCommandList::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md)

