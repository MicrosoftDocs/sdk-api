---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
title: D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
description: Specifies the configuration for video decoding.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS","D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS",""]
tech.root: mf
ms.assetid: bc59fda4-a50d-4e4e-abea-f539cfb7c8a7
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS, D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
 - d3d12video/D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS
---

# D3D12_VIDEO_DECODE_CONFIGURATION_FLAGS enumeration


## -description

Specifies the configuration for video decoding.

## -enum-fields

### -field D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_NONE 

No configuration flags.

### -field D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_HEIGHT_ALIGNMENT_MULTIPLE_32_REQUIRED 

The height of the output decoded surfaces must be a multiple of 32.

### -field D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_POST_PROCESSING_SUPPORTED 

The driver supports post processing. If this flag is set, the host decoder can set up post-processing by using the conversion flags in the <a href="ns-d3d12video-d3d12_video_decode_conversion_arguments.md">D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS</a>.

### -field D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_REFERENCE_ONLY_ALLOCATIONS_REQUIRED 

Reference resources must be allocated with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY</a>  resource flag.  References textures must be separate from output textures, similar to performing a format conversion or downscale.  This flag must not be set for [D3D12_VIDEO_DECODE_TIER_3](ne-d3d12video-d3d12_video_decode_tier.md) or greater.

### -field D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_ALLOW_RESOLUTION_CHANGE_ON_NON_KEY_FRAME 

The decode resolution can be changed on a non-key frame.

## -remarks

## -see-also