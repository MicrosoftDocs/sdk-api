---
UID: NS:d3d11_2.D3D11_TILE_SHAPE
title: D3D11_TILE_SHAPE (d3d11_2.h)
description: Describes the shape of a tile by specifying its dimensions. (D3D11_TILE_SHAPE)
helpviewer_keywords: ["D3D11_TILE_SHAPE","D3D11_TILE_SHAPE structure [Direct3D 11]","d3d11_2/D3D11_TILE_SHAPE","direct3d11.d3d11_tile_shape"]
old-location: direct3d11\d3d11_tile_shape.htm
tech.root: direct3d11
ms.assetid: B4B9D82C-2890-4CC4-AB5C-026FBD931B4E
ms.date: 12/05/2018
ms.keywords: D3D11_TILE_SHAPE, D3D11_TILE_SHAPE structure [Direct3D 11], d3d11_2/D3D11_TILE_SHAPE, direct3d11.d3d11_tile_shape
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_TILE_SHAPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILE_SHAPE
 - d3d11_2/D3D11_TILE_SHAPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_2.h
api_name:
 - D3D11_TILE_SHAPE
---

# D3D11_TILE_SHAPE structure


## -description

Describes the shape of a tile by specifying its dimensions.

## -struct-fields

### -field WidthInTexels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width in texels of the tile.

### -field HeightInTexels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The height in texels of the tile.

### -field DepthInTexels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The depth in texels of the tile.

## -remarks

Texels are equivalent to pixels.  For untyped buffer resources, a texel is just a byte. For multisample antialiasing (MSAA) surfaces, the numbers are still in terms of pixels/texels.
The values here are independent of the surface dimensions.  Even if the surface is smaller than what would fit in a tile, the full tile dimensions are reported here.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
