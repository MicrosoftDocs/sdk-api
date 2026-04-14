---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
ms.date: 04/07/2026
targetos: Windows
description: Contains motion vectors data for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
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
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_VECTORS
---

## -description

Contains motion vectors data with a union for either GPU texture or CPU buffer source. The user must check support for D3D12_FEATURE_VIDEO_ENCODER_MOTION_SEARCH before using this feature.

## -struct-fields

### -field MapSource

A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) indicating which source is used.

### -field pOpaqueLayoutBuffer

Use with D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE_GPU_TEXTURE. Pointer to an ID3D12Resource containing the resolved output in hardware-specific layout.

### -field pCPUBuffer

Use with D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE_CPU_BUFFER. Pointer to a [D3D12_VIDEO_ENCODER_MOVEREGION_INFO](ns-d3d12video-d3d12_video_encoder_moveregion_info.md).

## -remarks

## -see-also
