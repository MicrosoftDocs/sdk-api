---
UID: NE:d3d12video.D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS
title: D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS
ms.date: 11/4/2019
targetos: Windows
description: Specifies the motion estimation vector precision that a video encoder supports.
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
 - D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS
f1_keywords:
 - D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS
 - d3d12video/D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAGS
dev_langs:
 - c++
---

## -description

Specifies the motion estimation vector precision that a video encoder supports.

## -enum-fields

### -field D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAG_NONE:0

Vector precision is not supported by the encoder.

### -field D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_FLAG_QUARTER_PEL

The vector precision is quarter-pixel motion.

## -remarks

Query for supported vector precision values by calling [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) and specifying the feature value of [D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR](ne-d3d12video-d3d12_feature_video.md).

## -see-also

