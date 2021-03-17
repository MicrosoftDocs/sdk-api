---
UID: NS:d3d12video.D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
title: D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
ms.date: 11/4/2019
targetos: Windows
description: Specifies the input parameters for calls to ID3D12VideoEncodeCommandList::EstimateMotion.
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
req.typenames: D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
f1_keywords:
 - D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
 - d3d12video/D3D12_VIDEO_MOTION_ESTIMATOR_INPUT
dev_langs:
 - c++
---

## -description

Specifies the input parameters for calls to [ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md).

## -struct-fields

### -field pInputTexture2D

An [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md) representing the current frame. The motion estimation operation applies to the entire frame.

### -field InputSubresourceIndex

The base plane of the MIP and array slice to use for the input.

### -field pReferenceTexture2D

An [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md) representing the reference frame, or past frame, used for motion estimation.

### -field ReferenceSubresourceIndex

The base plane of the MIP and array slice to use for the reference.

### -field pHintMotionVectorHeap

An [ID3D12VideoMotionVectorHeap](nn-d3d12video-id3d12videomotionvectorheap.md) representing the buffer containing the hardware-dependent output of the previous motion estimator operation which may be used for hinting the current operation. This parameter may be NULL, indicating that previous motion estimator output should not be considered for the current operation.

## -remarks

## -see-also