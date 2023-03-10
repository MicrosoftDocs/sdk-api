---
UID: NS:d3d12video.D3D12_VIDEO_SCALE_SUPPORT
title: D3D12_VIDEO_SCALE_SUPPORT
description: Describes the supported scaling range of output sizes for a video scaler.
helpviewer_keywords: ["D3D12_VIDEO_SCALE_SUPPORT","D3D12_VIDEO_SCALE_SUPPORT",""]
tech.root: mf
ms.assetid: f05d3e73-5912-4d1b-92c1-fba067719001
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_SCALE_SUPPORT, D3D12_VIDEO_SCALE_SUPPORT,
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
req.typenames: D3D12_VIDEO_SCALE_SUPPORT
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_SCALE_SUPPORT
 - d3d12video/D3D12_VIDEO_SCALE_SUPPORT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_SCALE_SUPPORT
---

# D3D12_VIDEO_SCALE_SUPPORT structure


## -description

Describes the supported scaling range of output sizes for a video scaler.

## -struct-fields

### -field OutputSizeRange

A [D3D12_VIDEO_SIZE_RANGE](ns-d3d12video-d3d12_video_size_range.md) structure describing the supported output size range for the scaler.

### -field Flags

A member of the [D3D12_VIDEO_SCALE_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_scale_support_flags.md) enumeration specifying the supported scaling capabilities of the scaler.

## -remarks

By default, all possible output size combinations that exist between the maximum size and minimum size for the extent, inclusive, are supported.  *ScaleSupportFlags* may add additional restrictions to the supported scale sizes.  
When scaling is not supported, the minimum and maximum sizes should both be set to the input size and no flags should be specified.

## -see-also

