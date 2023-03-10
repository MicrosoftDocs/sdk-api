---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
ms.date: 06/10/2021
targetos: Windows
description: Represents codec configuration for HEVC encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC
dev_langs:
 - c++
---

## -description

Represents codec configuration for HEVC encoding.

## -struct-fields

### -field ConfigurationFlags

A bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAGS](ne-d3d12video-d3d12_video_encoder_codec_configuration_hevc_flags.md) enumeration defining the set of enabled codec features.

### -field MinLumaCodingUnitSize

A value from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE](ne-d3d12video-d3d12_video_encoder_codec_configuration_hevc_cusize.md) enumeration indicating the minimum luma coding block size to be used in the encoder. This value matches what the caller will code in SPS.

### -field MaxLumaCodingUnitSize

A value from the [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE](ne-d3d12video-d3d12_video_encoder_codec_configuration_hevc_cusize.md) enumeration indicating the maximum luma coding block size to be used in the encoder. This value matches what the caller will code in SPS.

### -field MinLumaTransformUnitSize

A value from the  [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE](ne-d3d12video-d3d12_video_encoder_codec_configuration_hevc_tusize.md) enumeration indicating the minimum luma transform block size to be used in the encoder. This value matches the pixel size of what the user will code in SPS.log2_min_luma_transform_block_size_minus2.

### -field MaxLumaTransformUnitSize

D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE

A value from the  [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE](ne-d3d12video-d3d12_video_encoder_codec_configuration_hevc_tusize.md) enumeration indicating the maximum luma transform block size to be used in the encoder. This value has to be consistent with the pixel size the user will code in SPS.log2_diff_max_min_luma_transform_block_size. The variable MaxTbLog2SizeY is set equal to log2_min_luma_transform_block_size_minus2 + 2 + log2_diff_max_min_luma_transform_block_size.

### -field max_transform_hierarchy_depth_inter

A UCHAR indicating the maximum hierarchy depth for transform units of coding units coded in inter prediction mode. The value of max_transform_hierarchy_depth_inter shall be in the range of 0 to CtbLog2SizeY − MinTbLog2SizeY, inclusive. The value indicated here must be consistent with the caller-coded SPS headers.

### -field max_transform_hierarchy_depth_intra

A UCHAR indicating the maximum hierarchy depth for transform units of coding units coded in intra prediction mode. The value of max_transform_hierarchy_depth_intra shall be in the range of 0 to CtbLog2SizeY − MinTbLog2SizeY, inclusive. The value indicated here must be consistent with the caller-coded SPS headers.

## -remarks

## -see-also

