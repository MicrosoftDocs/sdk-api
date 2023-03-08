---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList.EstimateMotion
title: ID3D12VideoEncodeCommandList::EstimateMotion
ms.date: 11/4/2019
targetos: Windows
description: Performs the motion estimation operation.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoEncodeCommandList::EstimateMotion
f1_keywords:
 - ID3D12VideoEncodeCommandList::EstimateMotion
 - d3d12video/ID3D12VideoEncodeCommandList::EstimateMotion
dev_langs:
 - c++
---

## -description

Performs the motion estimation operation.

## -parameters

### -param pMotionEstimator

An [ID3D12VideoMotionEstimator](nn-d3d12video-id3d12videomotionestimator.md) representing the video motion estimator context object.

### -param pOutputArguments

A [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](ns-d3d12video-d3d12_video_motion_estimator_output.md) structure representing the video motion estimation output arguments.

### -param pInputArguments

A [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](ns-d3d12video-d3d12_video_motion_estimator_input.md) structure representing the video motion estimation input arguments.

## -remarks

## -see-also

