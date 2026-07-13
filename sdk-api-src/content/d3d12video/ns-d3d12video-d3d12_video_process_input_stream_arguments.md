---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
title: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
description: Specifies input stream arguments for an input stream passed to ID3D12VideoCommandList::ProcessFrames.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS","D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS",""]
tech.root: mf
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS, D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS,
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
req.typenames: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
 - d3d12video/D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS
---

# D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS structure


## -description

Specifies input stream arguments for an input stream passed to [ID3D12VideoCommandList::ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).

## -struct-fields

### -field InputStream

An array of [D3D12_VIDEO_PROCESS_INPUT_STREAM](ns-d3d12video-d3d12_video_process_input_stream.md) structures containing the set of references for video processing. If the stereo format is [D3D12_VIDEO_PROCESS_STEREO_FORMAT_SEPARATE](ne-d3d12video-d3d12_video_frame_stereo_format.md), then two sets of input streams must be supplied.  For all other stereo formats, the first set of reference must be supplied, and the second should be zero initialized.

### -field Transform

A [D3D12_VIDEO_PROCESS_TRANSFORM](ns-d3d12video-d3d12_video_process_transform.md) structure specifying the flip, rotation, scale and destination translation for the video input.

### -field Flags

A value from the [D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS](ne-d3d12video-d3d12_video_process_input_stream_flags.md) enumeration specifying the options for the input stream.

### -field RateInfo

A [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](ns-d3d12video-d3d12_video_process_input_stream_rate.md) structure specifying the framerate and input and output indices for framerate conversion and deinterlacing.

### -field FilterLevels

The level to apply for each enabled filter.  The filter level is specified in the order that filters appear in the [D3D12_VIDEO_PROCESS_FILTER_FLAGS](ne-d3d12video-d3d12_video_process_filter_flags.md) enumeration.  Specify 0 if a filter is not enabled or the filter index is reserved.

### -field AlphaBlending

 
A [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](ns-d3d12video-d3d12_video_process_alpha_blending.md) structure specifying the planar alpha for an input stream on the video processor.

## -remarks

## -see-also

-[D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_process_input_stream_arguments1.md)
-[ID3D12VideoProcessCommandList::ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md)

