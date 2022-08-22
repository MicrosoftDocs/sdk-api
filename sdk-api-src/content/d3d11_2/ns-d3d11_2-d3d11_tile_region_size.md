---
UID: NS:d3d11_2.D3D11_TILE_REGION_SIZE
title: D3D11_TILE_REGION_SIZE (d3d11_2.h)
description: Describes the size of a tiled region. (D3D11_TILE_REGION_SIZE)
helpviewer_keywords: ["D3D11_TILE_REGION_SIZE","D3D11_TILE_REGION_SIZE structure [Direct3D 11]","d3d11_2/D3D11_TILE_REGION_SIZE","direct3d11.d3d11_tile_region_size"]
old-location: direct3d11\d3d11_tile_region_size.htm
tech.root: direct3d11
ms.assetid: D4A93462-9A2F-416A-9CC1-AC24DFF35890
ms.date: 12/05/2018
ms.keywords: D3D11_TILE_REGION_SIZE, D3D11_TILE_REGION_SIZE structure [Direct3D 11], d3d11_2/D3D11_TILE_REGION_SIZE, direct3d11.d3d11_tile_region_size
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
req.typenames: D3D11_TILE_REGION_SIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILE_REGION_SIZE
 - d3d11_2/D3D11_TILE_REGION_SIZE
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
 - D3D11_TILE_REGION_SIZE
---

# D3D11_TILE_REGION_SIZE structure


## -description

Describes the size of a tiled region.

## -struct-fields

### -field NumTiles

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of tiles in the tiled region.

### -field bUseBox

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the runtime uses the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members to define the region. 

If <b>TRUE</b>, the runtime uses the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members to define the region. 

If <b>FALSE</b>, the runtime ignores the <b>Width</b>, <b>Height</b>, and <b>Depth</b> members and uses the <b>NumTiles</b> member to traverse tiles in the resource linearly across x, then y, then z (as applicable) and then spills over mipmaps/arrays in subresource order.  For example, use this technique to map an entire resource at once.

Regardless of whether you specify <b>TRUE</b> or <b>FALSE</b> for <b>bUseBox</b>, you use a <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a> structure to specify the starting location for the region within the resource as a separate parameter outside of this structure by using x, y, and z coordinates. 

When the region includes mipmaps that are packed with nonstandard tiling, <b>bUseBox</b> must be <b>FALSE</b> because tile dimensions are not standard and the app only knows a count of how many tiles are consumed by the packed area, which is per array slice.  The corresponding (separate) starting location parameter uses x to offset into the flat range of tiles in this case, and y and z coordinates must each be 0.

### -field Width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width of the tiled region, in tiles. Used for buffer and 1D, 2D, and 3D textures.

### -field Height

Type: <b>UINT16</b>

The height of the tiled region, in tiles. Used for 2D and 3D textures.

### -field Depth

Type: <b>UINT16</b>

The depth of the tiled region, in tiles. Used for 3D textures or arrays. For arrays, used for advancing in depth jumps to next slice of same mipmap size, which isn't contiguous in the subresource counting space if there are multiple mipmaps.

## -see-also

<a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>



<a href="/windows/desktop/direct3d11/tiled-resources">Tiled resources</a>
