---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
ms.date: 06/09/2021
targetos: Windows
description: Represents encoder codec configuration support for HEVC encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC
dev_langs:
 - c++
---

## -description

Represents encoder codec configuration support for HEVC encoding.

## -struct-fields

### -field SupportFlags

A bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC_FLAGS](ne-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc_flags.md) specifying which optional features are supported for the codec.

### -field MinLumaCodingUnitSize

The minimum luma coding block size requested. This value must match what the caller will code in the sequence parameter set (SPS).

### -field MaxLumaCodingUnitSize

The maximum luma coding block size requested. This value matches what the user will code in SPS.

### -field MinLumaTransformUnitSize

The minimum luma transform block size requested. This value matches the pixel size of what the user will code in SPS.log2_min_luma_transform_block_size_minus2.

### -field MaxLumaTransformUnitSize

The maximum luma transform block size requested. This value must be consistent with the pixel size the user will code in SPS.log2_diff_max_min_luma_transform_block_size. The variable MaxTbLog2SizeY is set equal to log2_min_luma_transform_block_size_minus2 + 2 + log2_diff_max_min_luma_transform_block_size.

### -field max_transform_hierarchy_depth_inter

The maximum hierarchy depth for transform units of coding units coded in inter prediction mode. The value of max_transform_hierarchy_depth_inter shall be in the range of 0 to CtbLog2SizeY − MinTbLog2SizeY, inclusive.

### -field max_transform_hierarchy_depth_intra

Specifies the maximum hierarchy depth for transform units of coding units coded in intra prediction mode. The value of max_transform_hierarchy_depth_intra shall be in the range of 0 to CtbLog2SizeY − MinTbLog2SizeY, inclusive.

## -remarks

## -see-also

