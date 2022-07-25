---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS
ms.date: 06/10/2021
targetos: Windows
description: Specifies configuration flags for H.264 video encoding.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAGS
dev_langs:
 - c++
---

## -description

Specifies configuration flags for H.264 video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAG_USE_CONSTRAINED_INTRAPREDICTION

Forces the encoding of each intra-coded block with residual data only from other intra-coded blocks, i.e. not from inter-coded blocks, in the frame. Check for support in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAG_CONSTRAINED_INTRAPREDICTION_SUPPORT](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_h264_flags.md). This refers to constrained_intra_pred_flag in the picture parameter set (PPS).

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAG_USE_ADAPTIVE_8x8_TRANSFORM

Enables the usage of adaptive 8x8 transform. Please check for support in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAG_ADAPTIVE_8x8_TRANSFORM_ENCODING_SUPPORT](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_h264_flags.md).

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAG_ENABLE_CABAC_ENCODING

Enables CABAC entropy coding. If turned off, will use CAVLC. Please check for support in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAG_CABAC_ENCODING_SUPPORT](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_h264_flags.md).

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_FLAG_ALLOW_REQUEST_INTRA_CONSTRAINED_SLICES

Allows the caller to request for each frame with a special flag in the picture control structure that the slices of such frame are coded independently from each other. This mode restricts the motion vector search range to the region box of the current slice, i.e. motion vectors outside the slice boundary can't be used.

## -remarks

## -see-also

