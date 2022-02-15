---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_INPUT_STREAM
title: D3D12_VIDEO_PROCESS_INPUT_STREAM
description: Contains input information for the video processor blend functionality.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_INPUT_STREAM","D3D12_VIDEO_PROCESS_INPUT_STREAM",""]
tech.root: mf
ms.assetid: fcc82c3d-61d9-481b-951f-998ca55b6a60
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_INPUT_STREAM, D3D12_VIDEO_PROCESS_INPUT_STREAM,
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
req.typenames: D3D12_VIDEO_PROCESS_INPUT_STREAM
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM
 - d3d12video/D3D12_VIDEO_PROCESS_INPUT_STREAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM
---

# D3D12_VIDEO_PROCESS_INPUT_STREAM structure


## -description

Contains input information for the video processor blend functionality.

## -struct-fields

### -field pTexture2D

An [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the current input field or frame.

### -field Subresource

The subresource index to use of the *pTexture2D* argument.

### -field ReferenceSet

A [D3D12_VIDEO_PROCESS_REFERENCE_SET](ns-d3d12video-d3d12_video_process_reference_set.md) containing the set of references for video processing. Some video processing algorithms require forward or backward frame references. For more information, see [D3D12_FEATURE_VIDEO_PROCESS_REFERENCE_INFO](ne-d3d12video-d3d12_feature_video.md).

## -remarks

## -see-also
