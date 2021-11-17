---
UID: NF:d3d12video.ID3D12VideoEncoderHeap.GetResolutionList
tech.root: mf
title: ID3D12VideoEncoderHeap::GetResolutionList
ms.date: 06/22/2021
targetos: Windows
description: Gets the resolution list associated with the video encoder heap.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoEncoderHeap::GetResolutionList
f1_keywords:
 - ID3D12VideoEncoderHeap::GetResolutionList
 - d3d12video/ID3D12VideoEncoderHeap::GetResolutionList
dev_langs:
 - c++
---

## -description

Gets the resolution list associated with the video encoder heap.

## -parameters

### -param ResolutionsListCount

The count of resolutions to retrieve. Get the number of resolutions with which the encoder heap was created by calling [ID3D12VideoEncoderHeap::GetResolutionListCount](nf-d3d12video-id3d12videoencoderheap-getresolutionlistcount.md).

### -param pResolutionList

Receives a pointer to an array of [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) structures representing the resolutions specified in the [D3D12_VIDEO_ENCODER_HEAP_DESC](ns-d3d12video-d3d12_video_encoder_heap_desc.md) passed into [ID3D12VideoDevice3::CreateVideoEncoderHeap](nf-d3d12video-id3d12videodevice3-createvideoencoderheap.md).

## -returns

Returns S_OK on success.

## -remarks

## -see-also

