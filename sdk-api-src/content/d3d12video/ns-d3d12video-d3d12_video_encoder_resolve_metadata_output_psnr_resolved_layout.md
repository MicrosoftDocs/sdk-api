---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
ms.date: 04/07/2026
targetos: Windows
description: Describes the resolved PSNR values for Y, U, and V components of an encoded frame or subregion.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT
---

## -description

Describes the resolved PSNR (Peak Signal-to-Noise Ratio) values for the Y, U, and V components of an encoded frame or subregion.

## -struct-fields

### -field PSNRY

The PSNR value for the Y (luma) component.

### -field PSNRU

The PSNR value for the U (chroma) component. Set to zero by the driver if not supported.

### -field PSNRV

The PSNR value for the V (chroma) component. Set to zero by the driver if not supported.

## -remarks

The number of available components is determined by [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements1.md). Components not supported by the driver are written as zero.

For subregion-level PSNR, the resolved buffer contains a packed array of this structure with one element per subregion.

## -see-also

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments1.md)

