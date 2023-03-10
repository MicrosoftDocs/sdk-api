---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS
ms.date: 06/09/2021
targetos: Windows
description: Specifies configuration support flags for HEVC video encoding.
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
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS
dev_langs:
 - c++
---

## -description

Specifies configuration support flags for HEVC video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_BFRAME_LTR_COMBINED_SUPPORT

Support for usage of B frames and long term references frames simultaneously.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_INTRA_SLICE_CONSTRAINED_ENCODING_SUPPORT

Support for slice-contrained encoding, in which every slice in a frame is encoded independently from other slices in the same frame. This mode restricts the motion vector search range to the region box of the current slice, e.g. motion vectors outside the slice boundary can't be used.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_CONSTRAINED_INTRAPREDICTION_SUPPORT

Support for constrained intraprediction, that if activated will force the encoding of each intra-coded block with residual data only from other intra-coded blocks, e.g. not from inter-coded blocks. This refers to constrained_intra_pred_flag in the picture parameter set (PPS).

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_SAO_FILTER_SUPPORT

Support for sample adaptive offset.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_ASYMETRIC_MOTION_PARTITION_SUPPORT

Support for asymmetric motion partition.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_ASYMETRIC_MOTION_PARTITION_REQUIRED

Asymmetric motion partition must be always enabled. If this flag is set, D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_ASYMETRIC_MOTION_PARTITION_SUPPORT must also be set.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_TRANSFORM_SKIP_SUPPORT

Support for transform skip.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_DISABLING_LOOP_FILTER_ACROSS_SLICES_SUPPORT

Support for disabling loop filter across slices.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAG_P_FRAMES_IMPLEMENTED_AS_LOW_DELAY_B_FRAMES

When this flag is set, indicates that when encoding frames with type [D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC_P_FRAME](ne-d3d12video-d3d12_video_encoder_frame_type_hevc.md), they will be written as low delay B-Frames in the compressed bitstream. When this flag is not set, indicates that P frames will be written in the compressed bitstream.

**Note** When operating under this mode, it is the caller's responsibility to code the correct frame type in AUD_NUT and other parts of the HEVC bitstream, taking into account that P frames will be treated as generalized B frames with only references to past frames in POC order. 

## -remarks

## -see-also

