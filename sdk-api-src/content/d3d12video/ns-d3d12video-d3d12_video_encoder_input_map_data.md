---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
tech.root: mf
title: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
ms.date: 04/07/2026
targetos: Windows
description: Contains input map data for the ResolveInputParamLayout operation.
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
req.typenames: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
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
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
f1_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
 - d3d12video/D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA
---

## -description

Contains the input map data along with the input type indicator for [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md). Contains a union that is selected based on the MapType field.

## -struct-fields

### -field MapType

A [D3D12_VIDEO_ENCODER_INPUT_MAP_TYPE](ne-d3d12video-d3d12_video_encoder_input_map_type.md) specifying the type of input map.

### -field Quantization

A [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX](ns-d3d12video-d3d12_video_encoder_input_map_data_quantization_matrix.md) used when MapType is D3D12_VIDEO_ENCODER_INPUT_MAP_TYPE_QUANTIZATION_MATRIX.

### -field DirtyRegions

A [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS](ns-d3d12video-d3d12_video_encoder_input_map_data_dirty_regions.md) used when MapType is D3D12_VIDEO_ENCODER_INPUT_MAP_TYPE_DIRTY_REGIONS.

### -field MotionVectors

A [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS](ns-d3d12video-d3d12_video_encoder_input_map_data_motion_vectors.md) used when MapType is D3D12_VIDEO_ENCODER_INPUT_MAP_TYPE_MOTION_VECTORS.

## -remarks

## -see-also
