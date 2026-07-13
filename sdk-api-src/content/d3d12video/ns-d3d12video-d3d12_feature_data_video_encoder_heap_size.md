---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
ms.date: 06/09/2021
targetos: Windows
description: Retrieves a value indicating if the specified codec is supported for video encoding as well as the L0 and L1 sizes of the heap object.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_HEAP_SIZE
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_HEAP_SIZE](ne-d3d12video-d3d12_feature_video.md). Retrieves a value indicating if the specified codec is supported for video encoding as well as the L0 and L1 sizes of the heap object.

## -struct-fields

### -field HeapDesc

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md) structure specifying the creation properties for a video encoder heap. The driver should map these creation properties to size and assume the maximum resolution allowed for such heap.

### -field IsSupported

Receives a boolean value indicating if the encoder creation properties provided in **HeapDesc** are supported.

### -field MemoryPoolL0Size

Receives the L0 size of the heap object. Memory Pool L0 is the memory pool “closest” to the GPU. In the case of UMA adapters, this is the amount of system memory used. For discrete adapters, this is the amount of discrete memory used.

### -field MemoryPoolL1Size

Receives the L1 size of the heap object. Memory Pool L1 is the memory pool “second closest” to the GPU. In the case of UMA adapters, this value is zero. In the case of discrete adapters, this is the amount of system memory used.

## -remarks

## -see-also

