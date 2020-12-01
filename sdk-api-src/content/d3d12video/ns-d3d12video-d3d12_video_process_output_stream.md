---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_OUTPUT_STREAM
title: D3D12_VIDEO_PROCESS_OUTPUT_STREAM
description: Represents the output stream for video processing commands.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_OUTPUT_STREAM","D3D12_VIDEO_PROCESS_OUTPUT_STREAM",""]
tech.root: mf
ms.assetid: 35be7733-1ac9-4754-8923-1637d364f681
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_OUTPUT_STREAM, D3D12_VIDEO_PROCESS_OUTPUT_STREAM,
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
req.typenames: D3D12_VIDEO_PROCESS_OUTPUT_STREAM
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM
 - d3d12video/D3D12_VIDEO_PROCESS_OUTPUT_STREAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_OUTPUT_STREAM
---

# D3D12_VIDEO_PROCESS_OUTPUT_STREAM structure


## -description

Represents the output stream for video processing commands.  Points to the target surface for the processing operation.

## -struct-fields

### -field pTexture2D

A pointer to a [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the output surfaces for the video process command.

### -field Subresource

The subresource indices to use within the resource specified *pTexture2D* resource.

## -remarks

## -see-also