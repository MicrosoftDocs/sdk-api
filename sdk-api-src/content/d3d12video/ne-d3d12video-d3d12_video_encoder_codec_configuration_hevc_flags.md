---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS
ms.date: 06/10/2021
targetos: Windows
description: Specifies configuration flags for HEVC video encoding.
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
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS
dev_langs:
 - c++
---

## -description

Specifies configuration flags for HEVC video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_DISABLE_LOOP_FILTER_ACROSS_SLICES

Disables loop filtering across slices.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ALLOW_REQUEST_INTRA_CONSTRAINED_SLICES

Allows the usage of the intra constrained slices flag in picture control. This mode restricts the motion vector search range to the region box of the current slice, i.e. motion vectors outside the slice boundary can't be used.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_SAO_FILTER

Enables the sample adaptive offset filter.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_LONG_TERM_REFERENCES

Enables the usage of long term references in the picture reference management structures for HEVC.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_USE_ASYMETRIC_MOTION_PARTITION

Enables asymetric motion partitioning.

**Note** If [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_ASYMETRIC_MOTION_PARTITION_REQUIRED](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc_flags.md) was reported, this flag must be enabled.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_TRANSFORM_SKIPPING

Enables transform skipping.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_USE_CONSTRAINED_INTRAPREDICTION

Enables constrained intra prediction. This refers to constrained_intra_pred_flag in the PPS.

## -remarks

## -see-also

