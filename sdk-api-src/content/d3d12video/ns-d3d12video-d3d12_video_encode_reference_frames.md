---
UID: NS:d3d12video.D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
tech.root: mf
title: D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
ms.date: 06/30/2021
targetos: Windows
description: Represents the reconstructed reference images for an encoding operation.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
f1_keywords:
 - D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
 - d3d12video/D3D12_VIDEO_ENCODE_REFERENCE_FRAMES
dev_langs:
 - c++
---

## -description

Represents the reconstructed reference images for an encoding operation.

## -struct-fields

### -field NumTexture2Ds

The number of textures in the *ppTexture2Ds* array.

### -field ppTexture2Ds

An array of [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md) textures containing the reference images.

### -field pSubresources

An array of subresource indices for the reference textures specified in *ppTexture2Ds*. NULL indicates that subresource 0 should be assumed for each resource.
With texture arrays within a single resource, the subresource indices point to the array index of the first resource plane. With an array of textures in individual resources, the subresource index is typically zero.


## -remarks

## -see-also

