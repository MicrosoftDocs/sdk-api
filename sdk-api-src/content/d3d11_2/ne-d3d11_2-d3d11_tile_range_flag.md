---
UID: NE:d3d11_2.D3D11_TILE_RANGE_FLAG
title: D3D11_TILE_RANGE_FLAG (d3d11_2.h)
description: Specifies a range of tile mappings to use with ID3D11DeviceContext2::UpdateTiles.
helpviewer_keywords: ["D3D11_TILE_RANGE_FLAG","D3D11_TILE_RANGE_FLAG enumeration [Direct3D 11]","D3D11_TILE_RANGE_NULL","D3D11_TILE_RANGE_REUSE_SINGLE_TILE","D3D11_TILE_RANGE_SKIP","d3d11_2/D3D11_TILE_RANGE_FLAG","d3d11_2/D3D11_TILE_RANGE_NULL","d3d11_2/D3D11_TILE_RANGE_REUSE_SINGLE_TILE","d3d11_2/D3D11_TILE_RANGE_SKIP","direct3d11.d3d11_tile_range_flag"]
old-location: direct3d11\d3d11_tile_range_flag.htm
tech.root: direct3d11
ms.assetid: 3bab77f9-f18b-4b30-a1d8-09409253bfca
ms.date: 12/05/2018
ms.keywords: D3D11_TILE_RANGE_FLAG, D3D11_TILE_RANGE_FLAG enumeration [Direct3D 11], D3D11_TILE_RANGE_NULL, D3D11_TILE_RANGE_REUSE_SINGLE_TILE, D3D11_TILE_RANGE_SKIP, d3d11_2/D3D11_TILE_RANGE_FLAG, d3d11_2/D3D11_TILE_RANGE_NULL, d3d11_2/D3D11_TILE_RANGE_REUSE_SINGLE_TILE, d3d11_2/D3D11_TILE_RANGE_SKIP, direct3d11.d3d11_tile_range_flag
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: D3D11_TILE_RANGE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILE_RANGE_FLAG
 - d3d11_2/D3D11_TILE_RANGE_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_2.h
api_name:
 - D3D11_TILE_RANGE_FLAG
---

# D3D11_TILE_RANGE_FLAG enumeration


## -description

Specifies a range of tile mappings to use with <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles">ID3D11DeviceContext2::UpdateTiles</a>.

## -enum-fields

### -field D3D11_TILE_RANGE_NULL:0x1

The tile range is <b>NULL</b>.

### -field D3D11_TILE_RANGE_SKIP:0x2

Skip the tile range.

### -field D3D11_TILE_RANGE_REUSE_SINGLE_TILE:0x4

Reuse a single tile in the tile range.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles">ID3D11DeviceContext2::UpdateTiles</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
