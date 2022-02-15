---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
ms.date: 06/10/2021
targetos: Windows
description: Represents a codec configuration structure for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION
dev_langs:
 - c++
---

## -description

Represents a codec configuration structure for video encoding.

## -struct-fields

### -field DataSize

The data size of the provided codec configuration structure.

### -field pH264Config

A pointer to a [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264](ns-d3d12video-d3d12_video_encoder_codec_configuration_h264.md) structure containing codec configuration parameters for H.264 encoding.

### -field pHEVCConfig

A pointer to a [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC](ns-d3d12video-d3d12_video_encoder_codec_configuration_hevc.md) structure containing codec configuration parameters for HEVC encoding.

## -remarks

## -see-also

