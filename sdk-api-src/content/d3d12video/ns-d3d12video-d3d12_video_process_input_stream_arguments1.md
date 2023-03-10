---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
title: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
description: Specifies input stream arguments for an input stream passed to ID3D12VideoProcessCommandList1::ProcessFrames1, which supports changing the field type for each call.
tech.root: mf
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1"]
ms.date: 4/26/2019
ms.keywords: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS1
---

## -description

Specifies input stream arguments for an input stream passed to [ID3D12VideoProcessCommandList1::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md), which supports changing the field type for each call.

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

### -field FieldType

A value from the [D3D12_VIDEO_FIELD_TYPE](ne-d3d12video-d3d12_video_field_type.md) enumeration specfying the interlaced field type of the input source. When working with mixed content, use [ID3D12VideoProcessCommandList1::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md) which supports changing the field type for each call.

## -remarks

## -see-also

-[D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_input_stream_arguments.md)
-[ID3D12VideoProcessCommandList1::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md)

