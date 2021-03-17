---
UID: NS:d3d12video.D3D12_VIDEO_MOTION_ESTIMATOR_DESC
title: D3D12_VIDEO_MOTION_ESTIMATOR_DESC
ms.date: 11/4/2019
targetos: Windows
description: Describes a ID3D12VideoMotionEstimator. Pass this structure into ID3D12VideoDevice1::CreateVideoMotionEstimator to create an instance of ID3D12VideoMotionEstimator.
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
req.typenames: D3D12_VIDEO_MOTION_ESTIMATOR_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_MOTION_ESTIMATOR_DESC
f1_keywords:
 - D3D12_VIDEO_MOTION_ESTIMATOR_DESC
 - d3d12video/D3D12_VIDEO_MOTION_ESTIMATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a [ID3D12VideoMotionEstimator](nn-d3d12video-id3d12videomotionestimator.md). Pass this structure into [ID3D12VideoDevice1::CreateVideoMotionEstimator](nf-d3d12video-id3d12videodevice1-createvideomotionestimator.md) to create an instance of **ID3D12VideoMotionEstimator**.

## -struct-fields

### -field NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field InputFormat

A value from the [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration specifying the format of the input and reference frames.

### -field BlockSize

A value from the [D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE](ne-d3d12video-d3d12_video_motion_estimator_search_block_size.md) enumeration specifying the search block size the video motion estimator will use.

### -field Precision

A value from the [D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION](ne-d3d12video-d3d12_video_motion_estimator_vector_precision.md) enumeration specifying the vector precision the video motion estimator will use.

### -field SizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure representing the minimum and maximum input and reference frame size, in pixels, that the motion estimator will accept.

## -remarks

Call [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) and specify [D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR](ne-d3d12video-d3d12_feature_video.md) as the feature to determine supported values.

## -see-also