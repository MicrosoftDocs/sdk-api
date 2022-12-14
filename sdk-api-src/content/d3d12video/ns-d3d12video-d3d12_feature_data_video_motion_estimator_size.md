---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
title: D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
ms.date: 11/4/2019
targetos: Windows
description: Describes the allocation size of a video motion estimator heap.
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE
dev_langs:
 - c++
---

## -description

Describes the allocation size of a video motion estimator heap.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, identifies the physical adapter of the device this operation applies to.

### -field InputFormat

A [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) structure specifying the format of the input and reference resources.

### -field BlockSize

A value from the [D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE](ne-d3d12video-d3d12_video_motion_estimator_search_block_size.md) specifying the search block size for motion estimation.

### -field Precision

A value from the [D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION](ne-d3d12video-d3d12_video_motion_estimator_vector_precision.md) specifying the search block size for motion estimation.

### -field SizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure representing the minimum and maximum input and reference frame size, in pixels, used by the motion estimator.

### -field Protected

TRUE if the motion estimator operates on protected resource input and produces protected output; otherwise, FALSE.

### -field MotionVectorHeapMemoryPoolL0Size

The allocation size of the motion vector heap in the L0 memory pool. L0 is the physical system memory pool. When the adapter is discrete/NUMA, this pool has greater bandwidth for the CPU and less bandwidth for the GPU. When the adapter is UMA, this pool is the only one which is valid. For more information, see [Residency](/windows/win32/direct3d12/residency).

### -field MotionVectorHeapMemoryPoolL1Size

The allocation size of the motion vector heap in the L1 memory pool. L1 is typically known as the physical video memory pool. L1 is only available when the adapter is discrete/NUMA, and has greater bandwidth for the GPU and cannot even be accessed by the CPU. When the adapter is UMA, this pool is not available. For more information, see [Residency](/windows/win32/direct3d12/residency).

### -field MotionEstimatorMemoryPoolL0Size

The allocation size of the motion estimator heap in the L0 memory pool. L0 is the physical system memory pool. When the adapter is discrete/NUMA, this pool has greater bandwidth for the CPU and less bandwidth for the GPU. When the adapter is UMA, this pool is the only one which is valid. For more information, see [Residency](/windows/win32/direct3d12/residency).

### -field MotionEstimatorMemoryPoolL1Size

The allocation size of the motion estimator heap in the L1 memory pool. L1 is typically known as the physical video memory pool. L1 is only available when the adapter is discrete/NUMA, and has greater bandwidth for the GPU and cannot even be accessed by the CPU. When the adapter is UMA, this pool is not available. For more information, see [Residency](/windows/win32/direct3d12/residency).

## -remarks

## -see-also