---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
ms.date: 04/07/2026
targetos: Windows
description: Describes per-resolution support for dirty regions.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_DIRTY_REGIONS
---

## -description

Defines the reported support for dirty regions as output for [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits1.md).

## -struct-fields

### -field DirtyRegionsSupportFlags

A combination of [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_dirty_regions_support_flags.md) indicating supported features.

### -field MapSourcePreferenceRanking

Output parameter. Indicates the driver preference ranking for the map source.

## -remarks

## -see-also
