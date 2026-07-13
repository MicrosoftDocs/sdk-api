---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
ms.date: 04/07/2026
targetos: Windows
description: Specifies support flags for dirty regions in video encoding.
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
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS
---

## -description

Specifies support flags for dirty regions in video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAG_NONE : 0x0

Indicates no support.

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAG_REPEAT_FRAME : 0x1

Indicates the driver supports setting FullFrameIdentical to TRUE in [D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO](ns-d3d12video-d3d12_video_encoder_dirty_rect_info.md) or [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS](ns-d3d12video-d3d12_video_encoder_input_map_data_dirty_regions.md).

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAG_DIRTY_REGIONS : 0x2

Indicates the driver supports setting FullFrameIdentical to FALSE in [D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO](ns-d3d12video-d3d12_video_encoder_dirty_rect_info.md) or [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS](ns-d3d12video-d3d12_video_encoder_input_map_data_dirty_regions.md).

### -field D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAG_DIRTY_REGIONS_REQUIRE_FULL_ROW : 0x4

Indicates that when the driver supports D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAG_DIRTY_REGIONS, the regions passed by the app must be full rows.

## -remarks

## -see-also
