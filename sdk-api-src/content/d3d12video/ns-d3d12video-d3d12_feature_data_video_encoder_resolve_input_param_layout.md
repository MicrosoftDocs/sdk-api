---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
ms.date: 04/07/2026
targetos: Windows
description: Provides data for checking ResolveInputParamLayout support.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is D3D12_FEATURE_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT. Reports support for [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field SessionInfo

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO](ns-d3d12video-d3d12_video_encoder_input_map_session_info.md) containing information pertaining to the encoding session.

### -field MapType

Input parameter. A [D3D12_VIDEO_ENCODER_INPUT_MAP_TYPE](ne-d3d12video-d3d12_video_encoder_input_map_type.md) specifying the type of input map.

### -field IsSupported

Output parameter. Indicates if the given input params for feature are supported.

### -field MaxResolvedBufferAllocationSize

Output parameter. Indicates the size of the allocation the user must make for the output opaque buffer result of the ResolveInputParamLayout operation.

## -remarks

## -see-also
