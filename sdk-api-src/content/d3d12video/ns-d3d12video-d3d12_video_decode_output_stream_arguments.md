---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
title: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
description: Specifies the parameters for the output stream for a video decode operation. (D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS","D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS",""]
tech.root: mf
ms.assetid: c614b7f3-dd5e-4415-a90b-2419bff17b61
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS, D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS,
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
req.typenames: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
 - d3d12video/D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS
---

# D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS structure


## -description

Specifies the parameters for the output stream for a video decode operation. [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_decode_output_stream_arguments1.md) is used for the same purpose, but provides an additional field for histograms.

## -struct-fields

### -field pOutputTexture2D

An [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the output texture.  If decode conversion is enabled, this texture will contain the post-conversion output.  If decode conversion is not enabled, this texture will contain the decode output.

### -field OutputSubresource

The index of the output subresource of *pOutputTexture2D* to use.  This allows you to specify array indices if the output is an array.

### -field ConversionArguments

 
An optional [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](ns-d3d12video-d3d12_video_decode_conversion_arguments.md) structure containing output conversion parameters.

## -remarks

## -see-also
