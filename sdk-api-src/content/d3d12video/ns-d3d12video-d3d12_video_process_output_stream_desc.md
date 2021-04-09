---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
title: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
description: Specifies output stream arguments for the output passed to ID3D12VideoProcessCommandList::ProcessFrames.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC","D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC",""]
tech.root: mf
ms.assetid: 45a8af3d-5e67-4bc0-a38b-f5b45298aea9
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC, D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC,
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
req.typenames: D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
 - d3d12video/D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC
---

# D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC structure


## -description

Specifies output stream arguments for the output passed to [ID3D12VideoProcessCommandList::ProcessFrames](nf-d3d12video-id3d12videoprocesscommandlist-processframes.md).

## -struct-fields

### -field Format

A [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) structure specifying the format of the output resources.

### -field ColorSpace

A [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) value that specifies the colorspace for the video processor output surface.

### -field AlphaFillMode

A value from the [D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE](ne-d3d12video-d3d12_video_process_alpha_fill_mode.md) enumeration specifying the alpha fill mode for data that the video processor writes to the render target.

### -field AlphaFillModeSourceStreamIndex

The zero-based index of an input stream. This parameter is used if *AlphaFillMode* is [D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_SOURCE_STREAM](ne-d3d12video-d3d12_video_process_alpha_fill_mode.md). Otherwise, the parameter is ignored.

### -field BackgroundColor

The video processor uses the background color to fill areas of the target rectangle that do not contain a video image. Areas outside the target rectangle are not affected.  The meaning of the values are specified by the *ColorSpace* parameter.

| BackgroundColor   | YCbCrA   | RGBA    |
|-------------------|----------|---------|
| BackgroundColor[0]| Y        | R       |
| BackgroundColor[1]| Cb       | G       |
| BackgroundColor[2]| Cr       | B       |
| BackgroundColor[3]| A        | A       |

### -field FrameRate

 
A [DXGI_RATIONAL](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational) structure specifying the frame rate of the output video stream.

### -field EnableStereo

 
If TRUE, stereo output is enabled. Otherwise, the video processor produces mono video frames.

## -remarks

## -see-also