---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
ms.date: 04/07/2026
targetos: Windows
description: Describes per-resolution support for motion search.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_MOTION_SEARCH
---

## -description

Defines the reported support for motion search as output for [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits1.md).

## -struct-fields

### -field MaxMotionHints

Indicates the maximum value supported for NumHintsPerPixel or NumMoveRegions.

### -field MinDeviation

For D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE, the minimum supported SearchDeviationLimit.

### -field MaxDeviation

For D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE, the maximum supported SearchDeviationLimit.

### -field MapSourcePreferenceRanking

Indicates the driver preference ranking for the map source.

### -field MotionUnitPrecisionSupportFlags

A combination of [D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_frame_input_motion_unit_precision_support_flags.md) reporting supported precision modes.

### -field MotionSearchSupportFlags

A combination of [D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_motion_search_support_flags.md) indicating supported features.

## -remarks

## -see-also
