---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_TRANSFORM
title: D3D12_VIDEO_PROCESS_TRANSFORM
description: Specifies transform parameters for video processing.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_TRANSFORM","D3D12_VIDEO_PROCESS_TRANSFORM",""]
tech.root: mf
ms.assetid: 1939e664-81b1-4138-8103-3d721e38d19a
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_TRANSFORM, D3D12_VIDEO_PROCESS_TRANSFORM,
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
req.typenames: D3D12_VIDEO_PROCESS_TRANSFORM
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_TRANSFORM
 - d3d12video/D3D12_VIDEO_PROCESS_TRANSFORM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_TRANSFORM
---

# D3D12_VIDEO_PROCESS_TRANSFORM structure


## -description

Specifies transform parameters for video processing. Used by the [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_input_stream_arguments.md) structure.

## -struct-fields

### -field SourceRectangle

Specifies the source rectangle of the transform. This is the portion of the input surface that is blitted to the destination surface. The source rectangle is given in pixel coordinates, relative to the input surface.

### -field DestinationRectangle

Specifies the destination rectangle of the transform. This is the portion of the output surface that receives the blit for this stream. The destination rectangle is given in pixel coordinates, relative to the output surface.

### -field Orientation

 
The rotation and flip operation to apply to the source.  Source and Destination rectangles are specified in post orientation coordinates.

## -remarks

For stereo formats, the orientation is applied before the stereo format is applied.

## -see-also

