---
UID: NS:d3d12.D3D12_TILE_REGION_SIZE
title: D3D12_TILE_REGION_SIZE (d3d12.h)
description: Describes the size of a tiled region. (D3D12_TILE_REGION_SIZE)
helpviewer_keywords: ["D3D12_TILE_REGION_SIZE","D3D12_TILE_REGION_SIZE structure","d3d12/D3D12_TILE_REGION_SIZE","direct3d12.d3d12_tile_region_size"]
old-location: direct3d12\d3d12_tile_region_size.htm
tech.root: direct3d12
ms.assetid: 6F71BD17-09B5-4638-9CD4-E2D3BBA97044
ms.date: 12/05/2018
ms.keywords: D3D12_TILE_REGION_SIZE, D3D12_TILE_REGION_SIZE structure, d3d12/D3D12_TILE_REGION_SIZE, direct3d12.d3d12_tile_region_size
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
req.typenames: D3D12_TILE_REGION_SIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TILE_REGION_SIZE
 - d3d12/D3D12_TILE_REGION_SIZE
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
 - D3D12_TILE_REGION_SIZE
---

# D3D12_TILE_REGION_SIZE structure


## -description

Describes the size of a tiled region.

## -struct-fields

### -field NumTiles

The number of tiles in the tiled region.

### -field UseBox

Specifies whether the runtime uses the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members to define the region.
            

If <b>TRUE</b>, the runtime uses the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members to define the region. In this case,  <b>NumTiles</b> should be equal to <b>Width</b> *  <b>Height</b> * <b>Depth</b>.

If <b>FALSE</b>, the runtime ignores the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members and uses the <b>NumTiles</b> member to traverse tiles in the resource linearly across x, then y, then z (as applicable) and then spills over mipmaps/arrays in subresource order.  For example, use this technique to map an entire resource at once.
            

Regardless of whether you specify <b>TRUE</b> or <b>FALSE</b> for <b>UseBox</b>, you use a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a> structure to specify the starting location for the region within the resource as a separate parameter outside of this structure by using x, y, and z coordinates.
            

When the region includes mipmaps that are packed with nonstandard tiling, <b>UseBox</b> must be <b>FALSE</b> because tile dimensions are not standard and the app only knows a count of how many tiles are consumed by the packed area, which is per array slice.  The corresponding (separate) starting location parameter uses x to offset into the flat range of tiles in this case, and y and z coordinates must each be 0.

### -field Width

The width of the tiled region, in tiles. Used for buffer and 1D, 2D, and 3D textures.

### -field Height

The height of the tiled region, in tiles. Used for 2D and 3D textures.

### -field Depth

The depth of the tiled region, in tiles. Used for 3D textures or arrays. For arrays, used for advancing in depth jumps to next slice of same mipmap size, which isn't contiguous in the subresource counting space if there are multiple mipmaps.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">CopyTiles</a>, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a> methods.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-tile-region-size">CD3DX12_TILE_REGION_SIZE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
