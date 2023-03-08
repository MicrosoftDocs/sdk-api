---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
ms.date: 07/07/2021
targetos: Windows
description: Defines subregions as slices for codecs that support this partitioning mode.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA_SLICES
dev_langs:
 - c++
---

## -description

Defines subregions as slices for codecs that support this partitioning mode.

## -struct-fields

### -field MaxBytesPerSlice

The maximum number of bytes per slice to be used. This field is used exclusively with [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_BYTES_PER_SUBREGION](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md).

### -field NumberOfCodingUnitsPerSlice

The number of squared blocks to be used per slice. The size in pixels of the squared regions can be calculated using the current resolution and [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.SubregionBlockPixelsSize](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) for the current frame resolution. This field is used exclusively with [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_SQUARE_UNITS_PER_SUBREGION_ROW_UNALIGNED](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md).

### -field NumberOfRowsPerSlice

The number of squared blocks rows per slice for the frame to be divided into. The size in pixels of the squared regions can be calculated using the current resolution and [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.SubregionBlockPixelsSize](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) for the current frame resolution. This field is used exclusively with [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_ROWS_PER_SUBREGION](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md).

### -field NumberOfSlicesPerFrame


The number of slices to divide the frame into. This field is used exclusively with [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE_UNIFORM_PARTITIONING_SUBREGIONS_PER_FRAME](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md).

## -remarks

For modes that imply a fixed number of slices, the number of slices selected must be less than indicated by [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.MaxSubregionsNumber](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) and the selected resolution.

## -see-also

