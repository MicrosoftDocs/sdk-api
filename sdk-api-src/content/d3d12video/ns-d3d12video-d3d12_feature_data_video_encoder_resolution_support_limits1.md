---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
ms.date: 04/07/2026
targetos: Windows
description: Describes per-resolution support limits for video encoding, including QPMap, dirty regions, and motion search.
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
req.target-min-winverclnt:
req.target-min-winversvr:
req.target-type:
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
req.umdf-ver:
req.unicode-ansi:
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1
---

## -description

Extends the existing resolution support limits to include per-resolution support for QPMap, dirty regions, and motion search features. Used as output per-resolution in [D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2](ns-d3d12video-d3d12_feature_data_video_encoder_support2.md).

## -struct-fields

### -field MaxSubregionsNumber

The maximum number of subregions per frame for the associated resolution.

### -field MaxIntraRefreshFrameDuration

The maximum number of frames for an intra-refresh cycle.

### -field SubregionBlockPixelsSize

The size in pixels of the subregion block.

### -field QPMapRegionPixelsSize

The size in pixels of the QPMap region block.

### -field QPMap

A [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_QPMAP](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_qpmap.md) output parameter with QPMap support details.

### -field DirtyRegions

A [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_dirty_regions.md) output parameter. Only reported when dirty regions are enabled and supported. Zeroed memory otherwise.

### -field MotionSearch

A [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_motion_search.md) output parameter. Only reported when motion search is enabled and supported. Zeroed memory otherwise.

## -remarks

## -see-also
