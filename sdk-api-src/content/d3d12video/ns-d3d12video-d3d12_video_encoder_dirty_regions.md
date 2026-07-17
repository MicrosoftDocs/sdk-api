---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_DIRTY_REGIONS
tech.root: mf
title: D3D12_VIDEO_ENCODER_DIRTY_REGIONS
ms.date: 04/07/2026
targetos: Windows
description: Contains dirty regions data for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_DIRTY_REGIONS
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
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS
f1_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS
 - d3d12video/D3D12_VIDEO_ENCODER_DIRTY_REGIONS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_REGIONS
---

## -description

Contains dirty regions data with a union for either GPU texture or CPU buffer source. The user must check support for D3D12_FEATURE_VIDEO_ENCODER_DIRTY_REGIONS before using this feature.

## -struct-fields

### -field MapSource

A [D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE](ne-d3d12video-d3d12_video_encoder_input_map_source.md) indicating which source is used.

### -field pOpaqueLayoutBuffer

Use with D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE_GPU_TEXTURE. Pointer to an ID3D12Resource containing the resolved output in hardware-specific layout.

### -field pCPUBuffer

Use with D3D12_VIDEO_ENCODER_INPUT_MAP_SOURCE_CPU_BUFFER. Pointer to a [D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO](ns-d3d12video-d3d12_video_encoder_dirty_rect_info.md).

## -remarks

## -see-also
