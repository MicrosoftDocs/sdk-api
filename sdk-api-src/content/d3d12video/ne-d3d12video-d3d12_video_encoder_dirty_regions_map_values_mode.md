---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
ms.date: 04/07/2026
targetos: Windows
description: Specifies the interpretation of dirty regions map values.
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
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE
---

## -description

Specifies the interpretation of dirty regions map values.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE_DIRTY : 0

Indicates that a non-zero value means the pixel is different, and zero means the pixel is identical. When applied to [D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO](ns-d3d12video-d3d12_video_encoder_dirty_rect_info.md), indicates the group of pixels inside the rect have this meaning.

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE_SKIP : 1

Indicates that a zero value means the pixel is different, and non-zero means the pixel is identical. When applied to [D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO](ns-d3d12video-d3d12_video_encoder_dirty_rect_info.md), indicates the group of pixels inside the rect have this meaning.

## -remarks

## -see-also
