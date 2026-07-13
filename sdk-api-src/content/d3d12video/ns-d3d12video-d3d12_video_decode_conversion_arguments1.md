---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
title: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
description: Specifies the parameters for decode output conversion. (D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1","D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1",""]
tech.root: mf
ms.assetid: c5e03c98-6c64-43fa-b71a-8c4038f221dd
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1, D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1
---

# D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1 structure


## -description

Specifies the parameters for decode output conversion.  [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](ns-d3d12video-d3d12_video_decode_conversion_arguments.md) is used for the same purpose, but does not contain fields for output width and output height.

## -struct-fields

### -field Enable

A boolean value indicating whether decode conversion should be used.

### -field pReferenceTexture2D

A pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) containing the native decoding output. When downsampling is enabled, the output at native decode resolution, color space, and format may be required for future decode submissions (as reference frames, for instance).

### -field ReferenceSubresource

The subresource index of the resource provided in *pDecodeTexture2D* to use.

### -field OutputColorSpace

A value from the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration specifying the target color space of the output.

### -field DecodeColorSpace

A value from the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration specifying the source-decoded color space before conversion.

### -field OutputWidth

The output width, in pixels.

### -field OutputHeight

The output width, in pixels.

## -remarks

## -see-also
