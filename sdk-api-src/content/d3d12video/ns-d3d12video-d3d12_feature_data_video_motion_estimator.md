---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
title: D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
ms.date: 11/4/2019
targetos: Windows
description: Provides data for calls to ID3D12VideoDevice::CheckFeatureSupport when the feature specified is D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Retrieves the motion estimation capabilities for a video encoder.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR](ne-d3d12video-d3d12_feature_video.md). Retrieves the motion estimation capabilities for a video encoder.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, identifies the physical adapter of the device this operation applies to.

### -field InputFormat

A [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) structure specifying the format of the input resources.

### -field BlockSizeFlags

A bitwise OR combination of values from the [D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_FLAGS](ne-d3d12video-d3d12_video_motion_estimator_search_block_size_flags.md) enumeration specifying the encoder's supported search block sizes for motion estimation.

### -field PrecisionFlags

A bitwise OR combination of values from the [D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS](ne-d3d12video-d3d12_video_motion_estimator_vector_precision_flags.md) enumeration specifying the encoder's supported vector precision for motion estimation.

### -field SizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure representing the minimum and maximum input size supported by the driver. The driver sets the fields of this structure to zero if motion estimation is unsupported.

## -remarks

When the format is not supported with motion estimation, *BlockSizeFlags* will be set to [D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_FLAG_NONE](ne-d3d12video-d3d12_video_motion_estimator_search_block_size_flags.md), *PrecisionFlags* will be set to [D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAG_NONE](ne-d3d12video-d3d12_video_motion_estimator_vector_precision_flags.md), and the *SizeRange* will be set to all zeros.

## -see-also