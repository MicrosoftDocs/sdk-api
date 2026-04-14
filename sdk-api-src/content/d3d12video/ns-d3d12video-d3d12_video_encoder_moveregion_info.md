---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_MOVEREGION_INFO
tech.root: mf
title: D3D12_VIDEO_ENCODER_MOVEREGION_INFO
ms.date: 04/07/2026
targetos: Windows
description: Contains CPU-buffer move region information for motion vectors.
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
req.typenames: D3D12_VIDEO_ENCODER_MOVEREGION_INFO
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
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO
f1_keywords:
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO
 - d3d12video/D3D12_VIDEO_ENCODER_MOVEREGION_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_MOVEREGION_INFO
---

## -description

Contains CPU-buffer move region information for the motion vectors feature. All pixels inside a move rect move in the same direction.

## -struct-fields

### -field NumMoveRegions

Number of elements in pMoveRegions.

### -field pMoveRegions

Pointer to an array of [D3D12_VIDEO_ENCODER_MOVE_RECT](ns-d3d12video-d3d12_video_encoder_move_rect.md) structures specifying move regions.

### -field MotionSearchModeConfiguration

A [D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG](ns-d3d12video-d3d12_video_encoder_frame_motion_search_mode_config.md) specifying how the motion input vectors are used.

### -field SourceDPBFrameReference

An index into the picture parameters DPB descriptor indicating which previous reference frame this move region refers to.

### -field MotionUnitPrecision

A [D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION](ne-d3d12video-d3d12_video_encoder_frame_input_motion_unit_precision.md) defining the numerical unit used in the move rect values.

### -field Flags

A combination of [D3D12_VIDEO_ENCODER_MOVEREGION_INFO_FLAGS](ne-d3d12video-d3d12_video_encoder_moveregion_info_flags.md).

## -remarks

## -see-also
