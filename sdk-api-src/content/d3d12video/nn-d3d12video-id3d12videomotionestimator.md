---
UID: NN:d3d12video.ID3D12VideoMotionEstimator
title: ID3D12VideoMotionEstimator
ms.date: 1/23/2020
targetos: Windows
description: This interface maintains context for video motion estimation operations.
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
 - ID3D12VideoMotionEstimator
f1_keywords:
 - ID3D12VideoMotionEstimator
 - d3d12video/ID3D12VideoMotionEstimator
dev_langs:
 - c++
---

## -description

This interface maintains context for video motion estimation operations.

## -remarks

Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](nf-d3d12video-id3d12videodevice1-createvideomotionestimator.md).

This interface is passed into calls to [ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md).

## -see-also

