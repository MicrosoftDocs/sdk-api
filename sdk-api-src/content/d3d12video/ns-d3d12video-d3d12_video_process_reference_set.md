---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_REFERENCE_SET
title: D3D12_VIDEO_PROCESS_REFERENCE_SET
description: Contains the reference frames needed to perform video processing.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_REFERENCE_SET","D3D12_VIDEO_PROCESS_REFERENCE_SET",""]
tech.root: mf
ms.assetid: 7dc125bb-252e-4530-b8c8-63d3b0f2dcce
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_REFERENCE_SET, D3D12_VIDEO_PROCESS_REFERENCE_SET,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_PROCESS_REFERENCE_SET
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_REFERENCE_SET
 - d3d12video/D3D12_VIDEO_PROCESS_REFERENCE_SET
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_REFERENCE_SET
---

# D3D12_VIDEO_PROCESS_REFERENCE_SET structure


## -description

Contains the reference frames needed to perform video processing.

## -struct-fields

### -field NumPastFrames

The number of past reference frames provided in *ppPastFrames*.

### -field ppPastFrames

A pointer to an array of [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) surfaces. The number of elements in the array is *NumPastFrames*.

### -field pPastSubresources

An array of subresource indices for the list of *ppPastFrames* textures.  NULL indicates subresource 0 for each resource.

### -field NumFutureFrames

The number of future reference frames provided in *ppPastFrames*.

### -field ppFutureFrames

A pointer to an array of [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) surfaces. The number of elements in the array is *NumFutureFrames*.

### -field pFutureSubresources

 
An array of subresource indices for the list of *ppFutureFrames* textures.  NULL indicates subresource 0 for each resource.

## -remarks

## -see-also

[D3D12_FEATURE_VIDEO_PROCESS_REFERENCE_INFO](ne-d3d12video-d3d12_feature_video.md)