---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_ARGUMENT_TYPE
title: D3D12_VIDEO_DECODE_ARGUMENT_TYPE
description: Specifies the argument type of a D3D12_VIDEO_DECODE_FRAME_ARGUMENT
helpviewer_keywords: ["D3D12_VIDEO_DECODE_ARGUMENT_TYPE","D3D12_VIDEO_DECODE_ARGUMENT_TYPE",""]
tech.root: mf
ms.assetid: e9b5e3dd-d04e-4df5-9427-53255fcff245
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_ARGUMENT_TYPE, D3D12_VIDEO_DECODE_ARGUMENT_TYPE,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_ARGUMENT_TYPE
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_ARGUMENT_TYPE
 - d3d12video/D3D12_VIDEO_DECODE_ARGUMENT_TYPE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_ARGUMENT_TYPE
---

# D3D12_VIDEO_DECODE_ARGUMENT_TYPE enumeration


## -description

Specifies the argument type of a [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](ns-d3d12video-d3d12_video_decode_frame_argument.md).

## -enum-fields

### -field D3D12_VIDEO_DECODE_ARGUMENT_TYPE_PICTURE_PARAMETERS 

The argument is a picture decoding parameter buffer.

### -field D3D12_VIDEO_DECODE_ARGUMENT_TYPE_INVERSE_QUANTIZATION_MATRIX 

The argument is an inverse quantization matrix buffer.

### -field D3D12_VIDEO_DECODE_ARGUMENT_TYPE_SLICE_CONTROL 

The argument is a slice control buffer.

### -field D3D12_VIDEO_DECODE_ARGUMENT_TYPE_MAX_VALID 

TBD

## -remarks

The values used with the argument type are defined by the DXVA specification for a given codec.

## -see-also

