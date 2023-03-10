---
UID: NF:d3d12video.ID3D12VideoDevice1.CreateVideoMotionEstimator
title: ID3D12VideoDevice1::CreateVideoMotionEstimator
description: Creates an ID3D12VideoMotionEstimator, which maintains context for video motion estimation operations.
tech.root: mf
ms.date: 4/26/2019
ms.keywords: ID3D12VideoDevice1::CreateVideoMotionEstimator
targetos: Windows
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D12VideoDevice1::CreateVideoMotionEstimator
 - d3d12video/ID3D12VideoDevice1::CreateVideoMotionEstimator
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice1::CreateVideoMotionEstimator
---

## -description

Creates an [ID3D12VideoMotionEstimator](nn-d3d12video-id3d12videomotionestimator.md), which maintains context for video motion estimation operations.

## -parameters

### -param pDesc

A [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](ns-d3d12video-d3d12_video_motion_estimator_desc.md) describing the parameters used for motion estimation. This structure contains both input and output fields.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the **ID3D12VideoMotionEstimator** interface.

### -param ppVideoMotionEstimator

A pointer to a memory block that receives a pointer to the **ID3D12VideoMotionEstimator** interface.

## -returns

This method returns HRESULT.

## -remarks

## -see-also
