---
UID: NF:d3d12.ID3D12GraphicsCommandList.CopyTiles
title: ID3D12GraphicsCommandList::CopyTiles (d3d12.h)
description: Copies tiles from buffer to tiled resource or vice versa. (ID3D12GraphicsCommandList.CopyTiles)
helpviewer_keywords: ["CopyTiles","CopyTiles method","CopyTiles method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","CopyTiles method","ID3D12GraphicsCommandList.CopyTiles","ID3D12GraphicsCommandList::CopyTiles","d3d12/ID3D12GraphicsCommandList::CopyTiles","direct3d12.id3d12graphicscommandlist_copytiles"]
old-location: direct3d12\id3d12graphicscommandlist_copytiles.htm
tech.root: direct3d12
ms.assetid: F770CE6B-DD70-4102-BEFD-3E46B9957F5E
ms.date: 12/05/2018
ms.keywords: CopyTiles, CopyTiles method, CopyTiles method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,CopyTiles method, ID3D12GraphicsCommandList.CopyTiles, ID3D12GraphicsCommandList::CopyTiles, d3d12/ID3D12GraphicsCommandList::CopyTiles, direct3d12.id3d12graphicscommandlist_copytiles
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::CopyTiles
 - d3d12/ID3D12GraphicsCommandList::CopyTiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.CopyTiles
---

# ID3D12GraphicsCommandList::CopyTiles


## -description

Copies tiles from buffer to tiled resource or vice versa.

## -parameters

### -param pTiledResource [in]

Type: <b>ID3D12Resource*</b>

A pointer to a tiled resource.

### -param pTileRegionStartCoordinate [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a>*</b>

A pointer to a
            <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the tiled resource.

### -param pTileRegionSize [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size">D3D12_TILE_REGION_SIZE</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size">D3D12_TILE_REGION_SIZE</a> structure that describes the size of the tiled region.

### -param pBuffer [in]

Type: <b>ID3D12Resource*</b>

A pointer to an <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> that represents a default, dynamic, or staging buffer.

### -param BufferStartOffsetInBytes

Type: <b>UINT64</b>

The offset in bytes into the buffer at <i>pBuffer</i> to start the operation.

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags">D3D12_TILE_COPY_FLAGS</a></b>

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags">D3D12_TILE_COPY_FLAGS</a>-typed values that are combined by using a bitwise OR operation and that identifies how to copy tiles.

## -remarks

<b>CopyTiles</b> drops write operations to 
		  unmapped areas and handles read operations from unmapped areas 
		  (except on Tier_1 tiled resources, 
		  where reading and writing unmapped areas is invalid - refer to <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier">D3D12_TILED_RESOURCES_TIER</a>).
      

If a copy operation involves writing to the same memory location multiple times because multiple locations in the 
		destination resource are mapped to the same tile memory, the resulting write operations to multi-mapped tiles are 
		non-deterministic and non-repeatable; that is, accesses to the tile memory happen in whatever order the hardware 
		happens to execute the copy operation. 

The tiles involved in the copy operation can't include tiles that contain packed mipmaps or results of the copy 
		  operation are undefined. To transfer data to and from mipmaps that the hardware packs into the one-or-more tiles that constitute the packed mips, you must 
		  use the standard (that is, non-tile specific) copy APIs 
		  like <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>.

<b>CopyTiles</b> does copy data in a slightly different pattern than the standard copy methods.

The memory layout of the tiles in the non-tiled buffer resource side of the copy operation is linear in memory within 64 KB tiles, which the hardware and driver swizzle and de-swizzle per tile as appropriate when they transfer to and from a tiled resource. For multisample antialiasing (MSAA) surfaces, the hardware and driver traverse each pixel's samples in sample-index order before they move to the next pixel. For tiles that are partially filled on the right side (for a surface that has a width not a multiple of tile width in pixels), the pitch and stride to move down a row is the full size in bytes of the number pixels that would fit across the tile if the tile was full. So, there can be a gap between each row of pixels in memory. Mipmaps that are smaller than a tile are not packed together in the linear layout, which might seem to be a waste of memory space, but as mentioned you can't use <b>CopyTiles</b> to copy to mipmaps that the hardware packs together. You can just use generic copy APIs, like <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>, to copy small mipmaps individually.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>



<a href="/windows/desktop/direct3d11/tiled-resources">Tiled resources</a>
