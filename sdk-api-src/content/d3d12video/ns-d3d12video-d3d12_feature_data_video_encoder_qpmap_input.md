---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
ms.date: 04/07/2026
targetos: Windows
description: Provides data for checking QPMap input support.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_QPMAP_INPUT
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_QPMAP_INPUT](ne-d3d12video-d3d12_feature_video.md).

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field SessionInfo

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO](ns-d3d12video-d3d12_video_encoder_input_map_session_info.md) containing information pertaining to the encoding session.

### -field MapSource

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) indicating which source the user intends to use.

### -field IsSupported

Output parameter. Indicates if the given value for feature is supported.

### -field MapSourcePreferenceRanking

Output parameter. Indicates the driver preference (allowed output range [0..1]) for the input *MapSource*. The lowest the value reported, the best performance for this *MapSource* input type.

### -field BlockSize

Output parameter. Indicates the pixel size of the blocks. When input is [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE_CPU_BUFFER](ne-d3d12video-d3d12_video_encoder_input_map_source.md), this must match the driver-reported [QPMapRegionPixelsSize](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) value.

## -remarks

## -see-also
