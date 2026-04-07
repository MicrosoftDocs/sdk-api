---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
tech.root: mf
title: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
ms.date: 04/07/2026
targetos: Windows
description: Contains motion vectors input data for GPU texture source.
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
req.typenames: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
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
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
f1_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
 - d3d12video/D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_MOTION_VECTORS
---

## -description

Contains motion vectors input map data for the GPU texture input path of [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -struct-fields

### -field MotionSearchModeConfiguration

A [D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG](ns-d3d12video-d3d12_video_encoder_frame_motion_search_mode_config.md) specifying how the motion input vectors will be used.

### -field NumHintsPerPixel

Number of motion vector hint maps. Each map provides an additional motion vector hint for each (x, y) pixel position.

### -field ppMotionVectorMaps

Pointer to an array of [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) textures. Each texture in *ppMotionVectorMaps*[i] represents the i-th motion vector hint for each (x, y) pixel position. The dimension must match the input texture frame. Each element is **DXGI_FORMAT_R16G16_SINT** where R16 is the horizontal component and G16 is the vertical component.

### -field pMotionVectorMapsSubresources

Subresource indices for when *ppMotionVectorMaps* is a texture array. NULL otherwise.

### -field ppMotionVectorMapsMetadata

Pointer to an array of **ID3D12Resource** textures. Each texture in *ppMotionVectorMapsMetadata*[i] represents the metadata for the i-th motion vector hint. Each element is **DXGI_FORMAT_R8_UINT** where R8 holds the reference frame index in the DPB. A value of 255 indicates the motion vector must be ignored by the driver.

### -field pMotionVectorMapsMetadataSubresources

Subresource indices for when *ppMotionVectorMapsMetadata* is a texture array. NULL otherwise.

### -field MotionUnitPrecision

A [D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION](ne-d3d12video-d3d12_video_encoder_frame_input_motion_unit_precision.md) defining the numerical unit used in the motion vector values.

### -field PictureControlConfiguration

Provides information to the driver about picture control associated with the frame that will be encoded with this motion info, such as reference lists and reordering depending on the codec.

## -remarks

## -see-also
