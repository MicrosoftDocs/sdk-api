---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE
ms.date: 06/09/2021
targetos: Windows
description: Specifies possible values for luma transform block sizes for HEVC.
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
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE
dev_langs:
 - c++
---

## -description

Specifies possible values for luma transform block sizes for HEVC. 

## -enum-fields

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_4x4

Indicates a luma transform block of pixel size 4.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_8x8

Indicates a luma transform block of pixel size 8.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_16x16

Indicates a luma transform block of pixel size 16.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_32x32

Indicates a luma transform block of pixel size 32.

## -remarks

These values can then be used to express HEVC variables such as MinTbLog2SizeY, MaxTbLog2SizeY.

## -see-also

