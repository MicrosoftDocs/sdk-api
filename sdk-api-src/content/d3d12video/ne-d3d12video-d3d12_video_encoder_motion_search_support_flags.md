---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
ms.date: 04/07/2026
targetos: Windows
description: Specifies support flags for motion search in video encoding.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS
---

## -description

Specifies support flags for motion search in video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAG_NONE : 0x0

Indicates no support for the given input parameters.

### -field D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAG_SUPPORTED : 0x1

Indicates support for the given input parameters.

### -field D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAG_MULTIPLE_HINTS : 0x2

For CPU buffer input, indicates that pMoveRegions can contain overlapping rects. For GPU texture input, indicates that NumHintsPerPixel can be greater than 1.

### -field D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAG_GPU_TEXTURE_MULTIPLE_REFERENCES : 0x4

Indicates that each GPU motion map can have motion vectors that point to different DPB indices. When supported, the values (not equal to 255) in ppMotionVectorMapsMetadata[i] can point to different reference indices in the DPB.

## -remarks

## -see-also
