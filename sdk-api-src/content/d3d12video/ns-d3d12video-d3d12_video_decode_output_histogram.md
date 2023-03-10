---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
title: D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
description: Represents the histogram output buffer for a single component.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM","D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM",""]
tech.root: mf
ms.assetid: af5643ac-4095-4d26-8dfe-ef882462d207
ms.date: 11/14/2019
ms.keywords: D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM, D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
 - d3d12video/D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM
---

# D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM structure


## -description

Represents the histogram output buffer for a single component.

## -struct-fields

### -field Offset

The offset location in *pBuffer* to write the component histogram.  Must be 256-byte aligned.  Set to zero when a component is disabled.

### -field pBuffer

And [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md) representing the target buffer for hardware to write the components histogram.  Set to a nullptr when the component histogram is disabled.

## -remarks

Histogram output buffers are provided in the *Histograms* field of the [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](ns-d3d12video-d3d12_video_decode_output_stream_arguments1.md) structure.


The following [D3D12_HEAP_FLAGS](../d3d12/ne-d3d12-d3d12_heap_flags.md) are allowed when allocating heaps for video decode histograms.

- D3D12_HEAP_FLAG_SHARED
- D3D12_HEAP_FLAG_ALLOW_DISPLAY
- D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER
- D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES
- D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES
- D3D12_HEAP_FLAG_HARDWARE_PROTECTED
- D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH

The following [D3D12_HEAP_FLAGS](../d3d12/ne-d3d12-d3d12_heap_flags.md) are not allowed when allocating heaps for video decode histograms.

- D3D12_HEAP_FLAG_DENY_BUFFERS
 
The following [D3D12_RESOURCE_FLAGS](../d3d12/ne-d3d12-d3d12_resource_flags.md) are allowed when allocating resources for video decode histograms.

- D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET
- D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS
- D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER
- D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS
- D3D12_RESOURCE_FLAG_ALLOW_TEXTURE_DATA_INHERITANCE

The following [D3D12_RESOURCE_FLAGS](../d3d12/ne-d3d12-d3d12_resource_flags.md) are not allowed when allocating resources for video decode histograms.

- D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL
- D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE
- D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY
- D3D12_RESOURCE_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURE_PLACEMENT
- D3D12_RESOURCE_FLAG_ALLOW_ONLY_RT_DS_TEXTURE_PLACEMENT

## -see-also