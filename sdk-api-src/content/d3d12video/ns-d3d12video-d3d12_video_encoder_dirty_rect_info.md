---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
tech.root: mf
title: D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
ms.date: 04/07/2026
targetos: Windows
description: Contains CPU-buffer dirty rect information for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
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
 - D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
f1_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
 - d3d12video/D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_DIRTY_RECT_INFO
---

## -description

Contains CPU-buffer dirty rectangle information for the dirty regions feature.

## -struct-fields

### -field FullFrameIdentical

Indicates the current frame is a repeat frame from the frame referenced by SourceDPBFrameReference. When TRUE, pDirtyRects must be NULL.

### -field MapValuesType

A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_MAP_VALUES_MODE](ne-d3d12video-d3d12_video_encoder_dirty_regions_map_values_mode.md) indicating the semantic of the values of pDirtyRects.

### -field NumDirtyRects

Number of elements in pDirtyRects.

### -field pDirtyRects

Pointer to an array of RECT structures. Each rect indicates pixels at those positions are different or identical to pixels in the same positions of the previous frame referenced by SourceDPBFrameReference.

### -field SourceDPBFrameReference

An index into the picture parameters DPB descriptor indicating which previous reference frame this dirty region refers to.

## -remarks

## -see-also
