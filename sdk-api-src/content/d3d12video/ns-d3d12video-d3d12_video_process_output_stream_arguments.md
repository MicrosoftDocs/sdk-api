---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
title: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
description: Specifies output stream arguments for the output passed to ID3D12VideoCommandList::ProcessFrames.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS","D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS",""]
tech.root: mf
ms.assetid: 3da18a1c-655d-4be7-b1d8-80ca866afb3f
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS, D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS,
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
req.typenames: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
 - d3d12video/D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS
---

# D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS structure


## -description

Specifies output stream arguments for the output passed to [ID3D12VideoCommandList::ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).

## -struct-fields

### -field OutputStream

An array of [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](ns-d3d12video-d3d12_video_process_output_stream.md) structures representing the output surfaces for the video process command.  If stereo output is enabled, index zero contains the left output while index 1 contains the right input.  If stereo output is not enabled, only index 0 is used to specify the output while index 1 should be set to nullptr.

### -field TargetRectangle

 
The target rectangle is the area within the destination surface where the output will be drawn. The target rectangle is given in pixel coordinates, relative to the destination surface.

## -remarks

## -see-also

