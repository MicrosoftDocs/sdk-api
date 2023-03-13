---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
title: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
description: Specifies the parameters for the output stream for a video decode operation. (D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1","D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1",""]
tech.root: mf
ms.assetid: 58343794-0bd9-4be9-80f2-8cb0eec80a27
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1, D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1,
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
req.typenames: D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1
---

# D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1 structure


## -description

Specifies the parameters for the output stream for a video decode operation. [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_decode_output_stream_arguments.md) is used for the same purpose, but does not provide a field for histograms.

## -struct-fields

### -field pOutputTexture2D

An [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the output texture.  If decode conversion is enabled, this texture will contain the post-conversion output.  If decode conversion is not enabled, this texture will contain the decode output.

### -field OutputSubresource

The index of the output subresource of *pOutputTexture2D* to use.  This allows you to specify array indices if the output is an array.

### -field ConversionArguments

An optional [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](ns-d3d12video-d3d12_video_decode_conversion_arguments.md) structure containing output conversion parameters.

### -field Histograms

An array of [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](ns-d3d12video-d3d12_video_decode_output_histogram.md) structures that are populated with histogram data. The maximum size of the array is 4.

## -remarks

## -see-also
