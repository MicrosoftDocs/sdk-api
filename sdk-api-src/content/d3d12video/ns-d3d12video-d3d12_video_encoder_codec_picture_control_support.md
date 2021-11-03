---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
ms.date: 06/09/2021
targetos: Windows
description: Represents picture control support structure for multiple codecs.
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
req.typenames: D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT
dev_langs:
 - c++
---

## -description

Represents picture control support structure for multiple codecs.

## -struct-fields

### -field DataSize

The data size of the provided picture control support structure.

### -field pH264Support

A pointer to a [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264](ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_h264.md) structure representing the picture control support structure for H.264 encoding.

### -field pHEVCSupport

A pointer to a [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_HEVC](ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_hevc.md) structure representing the picture control support structure for HEVC encoding.

## -remarks

## -see-also

