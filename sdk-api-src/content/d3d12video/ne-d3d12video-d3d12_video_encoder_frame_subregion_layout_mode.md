---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE
ms.date: 06/07/2021
targetos: Windows
description: Specifies video encoder frame subregion layout modes.
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
 - D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE
dev_langs:
 - c++
---

## -description

Specifies video encoder frame subregion layout modes.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_FULL_FRAME

Full frame output support.

### -field D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_BYTES_PER_SUBREGION

Frame subregions are set as a number of bytes per subregion.

### -field D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_SQUARE_UNITS_PER_SUBREGION_ROW_UNALIGNED

Frame subregions are set as a number of squared blocks per subregion. The number of squared blocks does not need to be multiple of a row size in squared blocks (e.g. if the subregions don't need to be row-aligned). To set row-aligned number of squared blocks per subregion, use the D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_ROWS_PER_SUBREGION or D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_SUBREGIONS_PER_FRAME mode.

### -field D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_ROWS_PER_SUBREGION

Frames are divided into a number of slices determined by the number of rows per slice. The size in pixels of the rows can be calculated using the current resolution and [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.SubregionBlockPixelsSize](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) for the current frame resolution.

### -field D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_SUBREGIONS_PER_FRAME

Frames are divided into the specified number of slices.

## -remarks

## -see-also

