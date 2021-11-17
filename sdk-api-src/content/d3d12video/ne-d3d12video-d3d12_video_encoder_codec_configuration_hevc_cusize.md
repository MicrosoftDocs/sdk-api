---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE
ms.date: 06/09/2021
targetos: Windows
description: Specifies possible values for luma coding block sizes for HEVC. 
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
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE
dev_langs:
 - c++
---

## -description

Specifies possible values for luma coding block sizes for HEVC. 

## -enum-fields

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_8x8

Luma coding block of pixel size 8.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_16x16

Luma coding block of pixel size 16.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_32x32

Luma coding block of pixel size 32.

### -field D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_64x64

Luma coding block of pixel size 64.

## -remarks

These values can be used to express HEVC variables such as MinCbSizeY, CtbLog2SizeY.

## -see-also

