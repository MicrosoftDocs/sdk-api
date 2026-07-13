---
UID: NS:d3d12video.D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
tech.root: mf
title: D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
ms.date: 04/07/2026
targetos: Windows
description: Provides data for checking dirty regions support.
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
req.typenames: D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
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
 - D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
f1_keywords:
 - D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
 - d3d12video/D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_ENCODER_DIRTY_REGIONS
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is D3D12_FEATURE_VIDEO_ENCODER_DIRTY_REGIONS.

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field SessionInfo

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO](ns-d3d12video-d3d12_video_encoder_input_map_session_info.md) containing information pertaining to the encoding session.

### -field MapSource

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) indicating which source the user intends to use.

### -field MapValuesType

Input parameter. A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE](ne-d3d12video-d3d12_video_encoder_dirty_regions_map_values_mode.md) specifying the desired dirty region map type to check support for.

### -field SupportFlags

Output parameter. A combination of [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_dirty_regions_support_flags.md) indicating supported features.

### -field MapSourcePreferenceRanking

Output parameter. Indicates the driver preference (allowed output range [0..1]) for the input MapSource. The lowest the value reported, the best performance for this MapSource input type.

## -remarks

## -see-also
