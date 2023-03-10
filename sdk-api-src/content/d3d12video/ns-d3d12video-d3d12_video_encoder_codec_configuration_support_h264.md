---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
ms.date: 06/09/2021
targetos: Windows
description: Represents encoder codec configuration support for H.264 encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264
dev_langs:
 - c++
---

## -description

Represents encoder codec configuration support for H.264 encoding.

## -struct-fields

### -field SupportFlags

A bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAGS](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_h264_flags.md) specifying which optional features are supported for the codec.

### -field DisableDeblockingFilterSupportedModes

A bitwise OR combination of flags specifying the allowed modes supported for disable_deblocking_filter_idc syntax for H264 spec.

## -remarks

## -see-also

