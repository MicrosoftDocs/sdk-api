---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
ms.date: 04/07/2026
targetos: Windows
description: Provides data for checking motion search support.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_MOTION_SEARCH
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is D3D12_FEATURE_VIDEO_ENCODER_MOTION_SEARCH.

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field SessionInfo

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO](ns-d3d12video-d3d12_video_encoder_input_map_session_info.md) containing information pertaining to the encoding session.

### -field MotionSearchMode

Input parameter. A [D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE](ne-d3d12video-d3d12_video_encoder_frame_motion_search_mode.md) specifying the desired motion search mode to check support for.

### -field MapSource

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) indicating which source the user intends to use.

### -field BidirectionalRefFrameEnabled

Input parameter. Indicates if the user will use the feature for bidirectional reference frames (for example, B frames for H264).

### -field SupportFlags

Output parameter. A combination of [D3D12_VIDEO_ENCODER_MOTION_SEARCH_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_motion_search_support_flags.md) indicating supported features.

### -field MaxMotionHints

Output parameter. Indicates the maximum value supported by the driver for NumHintsPerPixel on GPU texture mode or NumMoveRegions on CPU buffer mode.

### -field MinDeviation

Output parameter. For D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE, indicates the minimum value supported for SearchDeviationLimit.

### -field MaxDeviation

Output parameter. For D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE, indicates the maximum value supported for SearchDeviationLimit.

### -field MapSourcePreferenceRanking

Output parameter. Indicates the driver preference (allowed output range [0..1]) for the input MapSource. The lowest the value reported, the best performance for this MapSource input type.

### -field MotionUnitPrecisionSupport

Output parameter. A combination of [D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_frame_input_motion_unit_precision_support_flags.md) reporting supported precision modes for input vectors.

## -remarks

## -see-also
