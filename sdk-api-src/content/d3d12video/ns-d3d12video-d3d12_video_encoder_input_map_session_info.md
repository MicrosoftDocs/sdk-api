---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
tech.root: mf
title: D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
ms.date: 04/07/2026
targetos: Windows
description: Describes the encoding session information for input map operations.
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
req.typenames: D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
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
 - D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
f1_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
 - d3d12video/D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO
---

## -description

Describes encoding session information used in feature support queries and input map operations.

## -struct-fields

### -field Codec

A [D3D12_VIDEO_ENCODER_CODEC](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_video_encoder_codec) value specifying the codec.

### -field Profile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_profile_desc) specifying the profile.

### -field Level

A [D3D12_VIDEO_ENCODER_LEVEL_SETTING](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_setting) specifying the level.

### -field InputFormat

A DXGI_FORMAT value specifying the input format.

### -field InputResolution

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_desc) specifying the input resolution.

### -field CodecConfiguration

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration) specifying the codec configuration.

### -field SubregionFrameEncoding

A [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md) value specifying the subregion layout mode.

### -field SubregionFrameEncodingData

A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data) specifying the subregion layout data.

## -remarks

## -see-also
