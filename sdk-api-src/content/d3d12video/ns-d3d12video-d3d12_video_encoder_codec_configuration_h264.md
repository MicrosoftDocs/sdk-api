---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
ms.date: 06/10/2021
targetos: Windows
description: Represents codec configuration for H.264 encoding.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264
dev_langs:
 - c++
---

## -description

Represents codec configuration for H.264 encoding.

## -struct-fields

### -field ConfigurationFlags

A bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS](ne-d3d12video-d3d12_video_encoder_codec_configuration_h264_flags.md) enumeration defining the set of enabled codec features.

### -field DirectModeConfig

A value from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_DIRECT_MODES](ne-d3d12video-d3d12_video_encoder_codec_configuration_h264_direct_modes.md) enumeration specifying direct modes.

### -field DisableDeblockingFilterConfig

A value from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_SLICES_DEBLOCKING_MODES](ne-d3d12video-d3d12_video_encoder_codec_configuration_h264_slices_deblocking_modes.md) enumeration specifying configuration related to the disable_deblocking_filter_idc syntax from the H.264 specification.

## -remarks

## -see-also

