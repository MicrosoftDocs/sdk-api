---
UID: NE:d3d12.D3D12_FILTER_TYPE
title: D3D12_FILTER_TYPE (d3d12.h)
description: Specifies the type of magnification or minification sampler filters.
helpviewer_keywords: ["D3D12_FILTER_TYPE","D3D12_FILTER_TYPE enumeration","D3D12_FILTER_TYPE_LINEAR","D3D12_FILTER_TYPE_POINT","d3d12/D3D12_FILTER_TYPE","d3d12/D3D12_FILTER_TYPE_LINEAR","d3d12/D3D12_FILTER_TYPE_POINT","direct3d12.d3d12_filter_type"]
old-location: direct3d12\d3d12_filter_type.htm
tech.root: direct3d12
ms.assetid: 3988D194-97C7-46C7-829D-154891684D68
ms.date: 12/05/2018
ms.keywords: D3D12_FILTER_TYPE, D3D12_FILTER_TYPE enumeration, D3D12_FILTER_TYPE_LINEAR, D3D12_FILTER_TYPE_POINT, d3d12/D3D12_FILTER_TYPE, d3d12/D3D12_FILTER_TYPE_LINEAR, d3d12/D3D12_FILTER_TYPE_POINT, direct3d12.d3d12_filter_type
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_FILTER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FILTER_TYPE
 - d3d12/D3D12_FILTER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_FILTER_TYPE
---

# D3D12_FILTER_TYPE enumeration


## -description

Specifies the type of magnification or minification sampler filters.

## -enum-fields

### -field D3D12_FILTER_TYPE_POINT:0

Point filtering is used as a texture magnification or minification filter. The texel with coordinates nearest to the desired pixel value is used. The texture filter to be used between mipmap levels is nearest-point mipmap filtering. The rasterizer uses the color from the texel of the nearest mipmap texture.

### -field D3D12_FILTER_TYPE_LINEAR:1

Bilinear interpolation filtering is used as a texture magnification or minification filter. A weighted average of a 2 x 2 area of texels surrounding the desired pixel is used. The texture filter to use between mipmap levels is trilinear mipmap interpolation. The rasterizer linearly interpolates pixel color, using the texels of the two nearest mipmap textures.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a> structure. Also, refer to the remarks for <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter">D3D12_FILTER</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
