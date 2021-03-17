---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
title: D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
description: Specifies the parameters for the input stream for a video process operation.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC","D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC",""]
tech.root: mf
ms.assetid: 35fb7ed3-29a1-4473-b979-e4698eb8c6e7
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC, D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC,
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
req.typenames: D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
 - d3d12video/D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC
---

# D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC structure


## -description

Specifies the parameters for the input stream for a video process operation.

## -struct-fields

### -field Format

 
A value from the [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format of the input stream. In the case of stereo, this format is the format of both inputs.

### -field ColorSpace

A value from the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration specifying the color space of the video processor input and reference surfaces.

### -field SourceAspectRatio

A [DXGI_RATIONAL](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational) structure specifying the source aspect ratio.

### -field DestinationAspectRatio

A [DXGI_RATIONAL](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational) structure specifying the destination aspect ratio.

### -field FrameRate

A [DXGI_RATIONAL](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational) structure specifying the frame rate of the input video stream.

### -field SourceSizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure representing the size of the source rectangle. This argument specifies the input range size this video processor must support for [ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).  If a source size exceeds the range, the video processor must be recreated.

### -field DestinationSizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure representing the size of the destination rectangle. This argument specifies the destination range size this video processor must support for [ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).  If a source size exceeds the range, the video processor must be recreated.

### -field EnableOrientation

 
A boolean value specifying whether the video processor should support all [D3D12_VIDEO_PROCESS_ORIENTATION](ne-d3d12video-d3d12_video_process_orientation.md) for [ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).

### -field FilterFlags

A bitwise OR combination of one or more flags from the [D3D12_VIDEO_PROCESS_FILTER_FLAGS](ne-d3d12video-d3d12_video_process_filter_flags.md) enumeration specifying the filters to enable.

### -field StereoFormat

A value from the [D3D12_VIDEO_FRAME_STEREO_FORMAT](ne-d3d12video-d3d12_video_frame_stereo_format.md) enumeration specifies whether the stream is stereo or not. A value of **D3D12_VIDEO_PROCESS_STEREO_FORMAT_SEPARATE** indicates that there will be two sets of input textures, and two sets of references for the stereo interlaced case.

### -field FieldType

A value from the [D3D12_VIDEO_FIELD_TYPE](ne-d3d12video-d3d12_video_field_type.md) enumeration specfying the interlaced field type of the input source. When working with mixed content, use [ID3D12VideoProcessCommandList1::ProcessFrames1](nf-d3d12video-id3d12videoprocesscommandlist1-processframes1.md) which supports changing the field type for each call.

### -field DeinterlaceMode

A value from the [D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS](ne-d3d12video-d3d12_video_process_deinterlace_flags.md) enumeration specifying the deinterlace mode to use.

### -field EnableAlphaBlending

A boolean value specifying whether alpha blending is enabled. Alpha blending settings are provided to [ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md) with *AlphaBlending* the field of the [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_input_stream_arguments.md) structure.

### -field LumaKey

A [D3D12_VIDEO_PROCESS_LUMA_KEY](ns-d3d12video-d3d12_video_process_luma_key.md) structure specifying the luma key for an input stream on the video processor.

### -field NumPastFrames

An integer specifying the number of past reference frames.

### -field NumFutureFrames

An integer specifying the number of future reference frames.

### -field EnableAutoProcessing

A boolean value specifying wither automatic processing features are enabled for the video processor.

## -remarks

## -see-also