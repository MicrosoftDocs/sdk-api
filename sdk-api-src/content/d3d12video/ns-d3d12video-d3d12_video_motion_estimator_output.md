---
UID: NS:d3d12video.D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
title: D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
ms.date: 11/4/2019
targetos: Windows
description: Specifies the output parameters for calls to ID3D12VideoEncodeCommandList::EstimateMotion.
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
req.typenames: D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
f1_keywords:
 - D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
 - d3d12video/D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT
dev_langs:
 - c++
---

## -description

Specifies the output parameters for calls to [ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md).

## -struct-fields

### -field pMotionVectorHeap

An [ID3D12VideoMotionVectorHeap](nn-d3d12video-id3d12videomotionvectorheap.md) containing the resolved motion estimation vectors. Motion vectors are resolved to a [DXGI_FORMAT_R16G16_SINT](../dxgiformat/ne-dxgiformat-dxgi_format.md) 2D texture. The resolved data is a signed 16-byte integer with quarter PEL units with the X vector component stored in the R component and the Y vector component stored in the G component. Motion vectors are stored in a 2D layout that corresponds to the pixel layout of the original input textures.

## -remarks

Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap.md) to translate the motion vector output of the [EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md) method from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.

## -see-also

[ID3D12VideoEncodeCommandList::EstimateMotion](nf-d3d12video-id3d12videoencodecommandlist-estimatemotion.md)
[ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap.md)
