---
UID: NE:d3d11_2.D3D11_TILE_COPY_FLAG
title: D3D11_TILE_COPY_FLAG (d3d11_2.h)
description: Identifies how to copy a tile.
helpviewer_keywords: ["D3D11_TILE_COPY_FLAG","D3D11_TILE_COPY_FLAG enumeration [Direct3D 11]","D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE","D3D11_TILE_COPY_NO_OVERWRITE","D3D11_TILE_COPY_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER","d3d11_2/D3D11_TILE_COPY_FLAG","d3d11_2/D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE","d3d11_2/D3D11_TILE_COPY_NO_OVERWRITE","d3d11_2/D3D11_TILE_COPY_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER","direct3d11.d3d11_tile_copy_flags"]
old-location: direct3d11\d3d11_tile_copy_flags.htm
tech.root: direct3d11
ms.assetid: 1ACBABF2-A0C5-419B-9723-BD0FEEEDF478
ms.date: 12/05/2018
ms.keywords: D3D11_TILE_COPY_FLAG, D3D11_TILE_COPY_FLAG enumeration [Direct3D 11], D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, D3D11_TILE_COPY_NO_OVERWRITE, D3D11_TILE_COPY_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, d3d11_2/D3D11_TILE_COPY_FLAG, d3d11_2/D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, d3d11_2/D3D11_TILE_COPY_NO_OVERWRITE, d3d11_2/D3D11_TILE_COPY_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, direct3d11.d3d11_tile_copy_flags
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
req.typenames: D3D11_TILE_COPY_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILE_COPY_FLAG
 - d3d11_2/D3D11_TILE_COPY_FLAG
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
 - D3D11_TILE_COPY_FLAG
---

# D3D11_TILE_COPY_FLAG enumeration


## -description

Identifies how to copy a tile.

## -enum-fields

### -field D3D11_TILE_COPY_NO_OVERWRITE:0x1

Indicates that the GPU isn't currently referencing any of the 
 portions of destination memory being written.

### -field D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE:0x2

Indicates that the <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">ID3D11DeviceContext2::CopyTiles</a> operation involves copying a linear buffer to a swizzled tiled resource. This means to copy tile data from the 
specified buffer location, reading tiles sequentially,
to the specified tile region (in x,y,z order if the region is a box), swizzling to optimal hardware memory layout as needed.
In this <b>ID3D11DeviceContext2::CopyTiles</b> call, you specify the source data with the  <i>pBuffer</i> parameter and the destination with the <i>pTiledResource</i> parameter.

### -field D3D11_TILE_COPY_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER:0x4

Indicates that the <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">ID3D11DeviceContext2::CopyTiles</a> operation involves copying a swizzled tiled resource to a linear buffer. This means to copy tile data from the tile region, reading tiles sequentially (in x,y,z order if the region is a box),
to the specified buffer location, deswizzling to linear memory layout as needed.
In this <b>ID3D11DeviceContext2::CopyTiles</b> call, you specify the source data with the <i>pTiledResource</i> parameter and the destination with the  <i>pBuffer</i> parameter.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
