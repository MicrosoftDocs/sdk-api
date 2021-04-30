---
UID: NN:d3d12video.ID3D12VideoMotionVectorHeap
title: ID3D12VideoMotionVectorHeap
ms.date: 1/23/2020
targetos: Windows
description: Represents a heap in which estimated motion vectors are stored.
tech.root: mf
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoMotionVectorHeap
f1_keywords:
 - ID3D12VideoMotionVectorHeap
 - d3d12video/ID3D12VideoMotionVectorHeap
dev_langs:
 - c++
---

## -description

Represents the storage of the motion vector output of a motion estimation operation in an IHV-dependent layout. Call [ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md) to calculate and store motion vectors. Use [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap.md) to copy and translate these results into the API-defined layout in a Texture 2D.

## -remarks

Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap.md).

This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](ns-d3d12video-d3d12_video_motion_estimator_output.md) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md). It is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](ns-d3d12video-d3d12_video_motion_estimator_input.md) structure.

## -see-also

