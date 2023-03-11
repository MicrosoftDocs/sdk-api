---
UID: NE:d3d12video.D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE
title: D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE
ms.date: 11/4/2019
targetos: Windows
description: Defines supported search block sizes for video motion estimation.
tech.root: mf
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE
f1_keywords:
 - D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE
 - d3d12video/D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE
dev_langs:
 - c++
---

## -description

Defines search block sizes for video motion estimation.

## -enum-fields

### -field D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_8X8:0

The search block size is 8x8 pixels.

### -field D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16:1

The search block size is 16x16 pixels.

## -remarks

Query for supported block sizes by calling [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) and specifying the feature value of [D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR](ne-d3d12video-d3d12_feature_video.md).

Set the desired block size for video motion estimation with the [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](ns-d3d12video-d3d12_video_motion_estimator_desc.md) passed into [ID3D12VideoDevice1::CreateVideoMotionEstimator](nf-d3d12video-id3d12videodevice1-createvideomotionestimator.md).

## -see-also

