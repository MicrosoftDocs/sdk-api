---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
ms.date: 04/07/2026
targetos: Windows
description: Provides data for calls to ID3D12VideoDevice::CheckFeatureSupport when the feature specified is D3D12_FEATURE_VIDEO_ENCODER_HEAP_SIZE1.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
req.umdf-ver: 
req.unicode-ansi: 
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE1
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_HEAP_SIZE1](ne-d3d12video-d3d12_feature_video.md). Extends [D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE](ns-d3d12video-d3d12_feature_data_video_encoder_heap_size.md) by passing [D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md) instead of [D3D12_VIDEO_ENCODER_HEAP_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md).

## -struct-fields

### -field HeapDesc

Input parameter. A [D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md) structure specifying the creation properties for a video encoder heap. The driver should map these creation properties to size and assume the maximum resolution allowed for such heap.

### -field IsSupported

Output parameter. Receives a boolean value indicating if the encoder creation properties provided in *HeapDesc* are supported.

### -field MemoryPoolL0Size

Output parameter. Receives the L0 size of the heap object. Memory Pool L0 is the memory pool "closest" to the GPU. In the case of UMA adapters, this is the amount of system memory used. For discrete adapters, this is the amount of discrete memory used.

### -field MemoryPoolL1Size

Output parameter. Receives the L1 size of the heap object. Memory Pool L1 is the memory pool "second closest" to the GPU. In the case of UMA adapters, this value is zero. In the case of discrete adapters, this is the amount of system memory used.

## -remarks

## -see-also

[D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE](ns-d3d12video-d3d12_feature_data_video_encoder_heap_size.md)
