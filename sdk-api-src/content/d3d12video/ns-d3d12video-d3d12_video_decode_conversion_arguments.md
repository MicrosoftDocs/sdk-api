---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
title: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
description: Specifies the parameters for decode output conversion. (D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS","D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS",""]
tech.root: mf
ms.assetid: 6a1fdbcd-abd7-431c-8cef-22f67b52ff0a
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS, D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS,
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
req.typenames: D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
 - d3d12video/D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS
---

# D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS structure


## -description

Specifies the parameters for decode output conversion. [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](ns-d3d12video-d3d12_video_decode_conversion_arguments.md) is used for the same purpose, but provides additional fields for output width and output height.

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

## -remarks

Scaling is specified by the difference between the native decode texture size and the output texture size.

Use [D3D12_FEATURE_VIDEO_DECODE_CONVERSION_SUPPORT](ne-d3d12video-d3d12_feature_video.md) to determine if a conversion combination is supported.

The source and destination resolution and format are communicated by the resource properties of decode textures and the output buffer specified in [ID3D12VideoCommandList::DecodeFrame](nf-d3d12video-id3d12videodecodecommandlist-decodeframe.md).

## -see-also
