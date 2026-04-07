---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
tech.root: mf
title: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
ms.date: 04/07/2026
targetos: Windows
description: Contains dirty regions input data for GPU texture source.
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
req.typenames: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
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
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
f1_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
 - d3d12video/D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_DIRTY_REGIONS
---

## -description

Contains dirty regions input map data for the GPU texture input path of [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -struct-fields

### -field FullFrameIdentical

Indicates that the current frame is a repeat frame from the frame referenced by SourceDPBFrameReference. When TRUE, pDirtyRegionsMap must be NULL.

### -field MapValuesType

A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE](ne-d3d12video-d3d12_video_encoder_dirty_regions_map_values_mode.md) indicating the semantic of the values of pDirtyRegionsMap.

### -field pDirtyRegionsMap

Pointer to an ID3D12Resource texture with the same dimensions as the input frame and format DXGI_FORMAT_R8_UINT. Each (x, y) position indicates if the pixel at that position is different or identical to a pixel in the same position of the previous frame in the DPB used as reference.

### -field SourceDPBFrameReference

An index into the picture parameters DPB descriptor indicating which previous reference frame this dirty region refers to.

## -remarks

## -see-also
