---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
ms.date: 04/07/2026
targetos: Windows
description: Describes picture control properties for a video encode operation.
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
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
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
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC1
---

## -description

Describes the picture control properties for a video encode operation, including support for quantization maps, dirty regions, and motion vectors.

## -struct-fields

### -field IntraRefreshFrameIndex

The current frame index in an intra-refresh cycle.

### -field Flags

A combination of [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md).

### -field PictureControlCodecData

Codec-specific picture control data as a [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA1](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data1.md).

### -field ReferenceFrames

A [D3D12_VIDEO_ENCODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encode_reference_frames) specifying the reference frames.

### -field MotionVectors

A [D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS](ns-d3d12video-d3d12_video_encoder_frame_motion_vectors.md) with motion vector input data. Requires [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_ENABLE_MOTION_VECTORS_INPUT](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md).

### -field DirtyRects

A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS](ns-d3d12video-d3d12_video_encoder_dirty_regions.md) with dirty regions input data. Requires [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_ENABLE_DIRTY_REGIONS_INPUT](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md).

### -field QuantizationTextureMap

A [D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP](ns-d3d12video-d3d12_video_encoder_quantization_opaque_map.md) with the GPU quantization map. Requires [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_ENABLE_QUANTIZATION_MATRIX_INPUT](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md).

## -remarks

## -see-also
