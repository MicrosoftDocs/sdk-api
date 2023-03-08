---
UID: NS:d3d12.D3D12_TILE_SHAPE
title: D3D12_TILE_SHAPE (d3d12.h)
description: Describes the shape of a tile by specifying its dimensions. (D3D12_TILE_SHAPE)
helpviewer_keywords: ["D3D12_TILE_SHAPE","D3D12_TILE_SHAPE structure","d3d12/D3D12_TILE_SHAPE","direct3d12.d3d12_tile_shape"]
old-location: direct3d12\d3d12_tile_shape.htm
tech.root: direct3d12
ms.assetid: 9FCF949C-B2B8-404F-9E4C-8CC6B636B687
ms.date: 12/05/2018
ms.keywords: D3D12_TILE_SHAPE, D3D12_TILE_SHAPE structure, d3d12/D3D12_TILE_SHAPE, direct3d12.d3d12_tile_shape
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
req.typenames: D3D12_TILE_SHAPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TILE_SHAPE
 - d3d12/D3D12_TILE_SHAPE
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
 - D3D12_TILE_SHAPE
---

# D3D12_TILE_SHAPE structure


## -description

Describes the shape of a tile by specifying its dimensions.

## -struct-fields

### -field WidthInTexels

The width in texels of the tile.

### -field HeightInTexels

The height in texels of the tile.

### -field DepthInTexels

The depth in texels of the tile.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling">GetResourceTiling</a>     method.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-tile-shape">CD3DX12_TILE_SHAPE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
