---
UID: NE:d3d10.D3D10_FILTER_TYPE
title: D3D10_FILTER_TYPE (d3d10.h)
description: Types of magnification or minification sampler filters.
helpviewer_keywords: ["137ceae1-1546-228a-f67c-1e9ba1c8ef29","D3D10_FILTER_TYPE","D3D10_FILTER_TYPE enumeration [Direct3D 10]","D3D10_FILTER_TYPE_LINEAR","D3D10_FILTER_TYPE_POINT","d3d10/D3D10_FILTER_TYPE","d3d10/D3D10_FILTER_TYPE_LINEAR","d3d10/D3D10_FILTER_TYPE_POINT","direct3d10.d3d10_filter_type"]
old-location: direct3d10\d3d10_filter_type.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_filter_type.htm
ms.date: 12/05/2018
ms.keywords: 137ceae1-1546-228a-f67c-1e9ba1c8ef29, D3D10_FILTER_TYPE, D3D10_FILTER_TYPE enumeration [Direct3D 10], D3D10_FILTER_TYPE_LINEAR, D3D10_FILTER_TYPE_POINT, d3d10/D3D10_FILTER_TYPE, d3d10/D3D10_FILTER_TYPE_LINEAR, d3d10/D3D10_FILTER_TYPE_POINT, direct3d10.d3d10_filter_type
req.header: d3d10.h
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
req.typenames: D3D10_FILTER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_FILTER_TYPE
 - d3d10/D3D10_FILTER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_FILTER_TYPE
---

# D3D10_FILTER_TYPE enumeration


## -description

Types of magnification or minification sampler filters.

## -enum-fields

### -field D3D10_FILTER_TYPE_POINT:0

Point filtering used as a texture magnification or minification filter. The texel with coordinates nearest to the desired pixel value is used. The texture filter to be used between mipmap levels is nearest-point mipmap filtering. The rasterizer uses the color from the texel of the nearest mipmap texture.

### -field D3D10_FILTER_TYPE_LINEAR:1

Bilinear interpolation filtering used as a texture magnification or minification filter. A weighted average of a 2 x 2 area of texels surrounding the desired pixel is used. The texture filter to use between mipmap levels is trilinear mipmap interpolation. The rasterizer linearly interpolates pixel color, using the texels of the two nearest mipmap textures.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
