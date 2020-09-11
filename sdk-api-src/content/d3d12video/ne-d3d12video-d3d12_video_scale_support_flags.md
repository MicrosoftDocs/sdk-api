---
UID: NE:d3d12video.D3D12_VIDEO_SCALE_SUPPORT_FLAGS
title: D3D12_VIDEO_SCALE_SUPPORT_FLAGS
description: Specifies the scaling capabilities of the video scaler.
helpviewer_keywords: ["D3D12_VIDEO_SCALE_SUPPORT_FLAGS","D3D12_VIDEO_SCALE_SUPPORT_FLAGS",""]
tech.root: mf
ms.assetid: 80535fbf-1159-4a7a-8452-5d2adf9363f0
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_SCALE_SUPPORT_FLAGS, D3D12_VIDEO_SCALE_SUPPORT_FLAGS,
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
req.typenames: D3D12_VIDEO_SCALE_SUPPORT_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_SCALE_SUPPORT_FLAGS
 - d3d12video/D3D12_VIDEO_SCALE_SUPPORT_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_SCALE_SUPPORT_FLAGS
---

# D3D12_VIDEO_SCALE_SUPPORT_FLAGS enumeration


## -description

Specifies the scaling capabilities of the video scaler.

## -enum-fields

### -field D3D12_VIDEO_SCALE_SUPPORT_FLAG_NONE 

All possible output size width/height combinations that exist between the maximum size and minimum size for the extent, inclusive, are supported.

### -field D3D12_VIDEO_SCALE_SUPPORT_FLAG_POW2_ONLY 

The scaler only supports output sizes at a power of two scale factors within the range.  The x and y scale factors must be the same for both dimensions when this flag is set.

### -field D3D12_VIDEO_SCALE_SUPPORT_FLAG_EVEN_DIMENSIONS_ONLY 

The scaler only supports output sizes with even output dimensions.

## -remarks

## -see-also

