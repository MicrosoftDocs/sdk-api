---
UID: NE:d3d12.D3D12_TILE_COPY_FLAGS
title: D3D12_TILE_COPY_FLAGS (d3d12.h)
description: Specifies how to copy a tile.
helpviewer_keywords: ["D3D12_TILE_COPY_FLAGS","D3D12_TILE_COPY_FLAGS enumeration","D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE","D3D12_TILE_COPY_FLAG_NONE","D3D12_TILE_COPY_FLAG_NO_HAZARD","D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER","d3d12/D3D12_TILE_COPY_FLAGS","d3d12/D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE","d3d12/D3D12_TILE_COPY_FLAG_NONE","d3d12/D3D12_TILE_COPY_FLAG_NO_HAZARD","d3d12/D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER","direct3d12.d3d12_tile_copy_flags"]
old-location: direct3d12\d3d12_tile_copy_flags.htm
tech.root: direct3d12
ms.assetid: A540A369-DF23-4961-8213-B4B2B5C365E5
ms.date: 12/05/2018
ms.keywords: D3D12_TILE_COPY_FLAGS, D3D12_TILE_COPY_FLAGS enumeration, D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, D3D12_TILE_COPY_FLAG_NONE, D3D12_TILE_COPY_FLAG_NO_HAZARD, D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, d3d12/D3D12_TILE_COPY_FLAGS, d3d12/D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, d3d12/D3D12_TILE_COPY_FLAG_NONE, d3d12/D3D12_TILE_COPY_FLAG_NO_HAZARD, d3d12/D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, direct3d12.d3d12_tile_copy_flags
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
req.typenames: D3D12_TILE_COPY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TILE_COPY_FLAGS
 - d3d12/D3D12_TILE_COPY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_TILE_COPY_FLAGS
---

# D3D12_TILE_COPY_FLAGS enumeration


## -description

Specifies how to copy a tile.

## -enum-fields

### -field D3D12_TILE_COPY_FLAG_NONE:0

No tile-copy flags are specified.

### -field D3D12_TILE_COPY_FLAG_NO_HAZARD:0x1

Indicates that the GPU isn't currently referencing any of the
            portions of destination memory being written.

### -field D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE:0x2

Indicates that the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">ID3D12GraphicsCommandList::CopyTiles</a> operation involves copying a linear buffer to a swizzled tiled resource. This means to copy tile data from the
            specified buffer location, reading tiles sequentially,
            to the specified tile region (in x,y,z order if the region is a box), swizzling to optimal hardware memory layout as needed.
            In this <b>ID3D12GraphicsCommandList::CopyTiles</b> call, you specify the source data with the  <i>pBuffer</i> parameter and the destination with the <i>pTiledResource</i> parameter.

### -field D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER:0x4

Indicates that the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">ID3D12GraphicsCommandList::CopyTiles</a> operation involves copying a swizzled tiled resource to a linear buffer. This means to copy tile data from the tile region, reading tiles sequentially (in x,y,z order if the region is a box),
            to the specified buffer location, deswizzling to linear memory layout as needed.
            In this <b>ID3D12GraphicsCommandList::CopyTiles</b> call, you specify the source data with the <i>pTiledResource</i> parameter and the destination with the  <i>pBuffer</i> parameter.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">CopyTiles</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
