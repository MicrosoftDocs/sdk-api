---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
title: D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
description: Describes the allocation size of a video decoder heap. (D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE)
tech.root: mf
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE"]
ms.date: 4/26/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE
---

## -description

Describes the allocation size of a video decoder heap.

## -struct-fields

### -field VideoDecoderHeapDesc

A [D3D12_VIDEO_DECODER_HEAP_DESC](ns-d3d12video-d3d12_video_decoder_heap_desc.md) describing a [ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md).

### -field MemoryPoolL0Size

The allocation size of the video decoder heap in the L0 memory pool. L0 is the physical system memory pool. When the adapter is discrete/NUMA, this pool has greater bandwidth for the CPU and less bandwidth for the GPU. When the adapter is UMA, this pool is the only one which is valid. For more information, see [Residency](/windows/win32/direct3d12/residency).

### -field MemoryPoolL1Size

The allocation size of the video decoder heap in the L1 memory pool. L1 is typically known as the physical video memory pool. L1 is only available when the adapter is discrete/NUMA, and has greater bandwidth for the GPU and cannot even be accessed by the CPU. When the adapter is UMA, this pool is not available. For more information, see [Residency](/windows/win32/direct3d12/residency).

## -remarks

## -see-also

[Residency](/windows/win32/direct3d12/residency)

