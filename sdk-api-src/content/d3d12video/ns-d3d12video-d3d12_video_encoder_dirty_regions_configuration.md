---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
tech.root: mf
title: D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
ms.date: 04/07/2026
targetos: Windows
description: Defines the configuration for dirty regions input.
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
req.typenames: D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
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
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
f1_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
 - d3d12video/D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION
---

## -description

Defines the configuration for dirty regions as input for [D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2](ns-d3d12video-d3d12_feature_data_video_encoder_support2.md).

## -struct-fields

### -field Enabled

Indicates if dirty regions are enabled.

### -field MapSource

A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) specifying the input source.

### -field MapValuesType

A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE](ne-d3d12video-d3d12_video_encoder_dirty_regions_map_values_mode.md) specifying the dirty region map type.

## -remarks

## -see-also
