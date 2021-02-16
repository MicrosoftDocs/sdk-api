---
UID: NF:d3d11_2.ID3D11DeviceContext2.UpdateTiles
title: ID3D11DeviceContext2::UpdateTiles (d3d11_2.h)
description: Updates tiles by copying from app memory to the tiled resource.
helpviewer_keywords: ["ID3D11DeviceContext2 interface [Direct3D 11]","UpdateTiles method","ID3D11DeviceContext2.UpdateTiles","ID3D11DeviceContext2::UpdateTiles","UpdateTiles","UpdateTiles method [Direct3D 11]","UpdateTiles method [Direct3D 11]","ID3D11DeviceContext2 interface","d3d11_2/ID3D11DeviceContext2::UpdateTiles","direct3d11.id3d11devicecontext2_updatetiles"]
old-location: direct3d11\id3d11devicecontext2_updatetiles.htm
tech.root: direct3d11
ms.assetid: EB0F9CBD-29B2-484D-8923-6686C73487F7
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],UpdateTiles method, ID3D11DeviceContext2.UpdateTiles, ID3D11DeviceContext2::UpdateTiles, UpdateTiles, UpdateTiles method [Direct3D 11], UpdateTiles method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::UpdateTiles, direct3d11.id3d11devicecontext2_updatetiles
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext2::UpdateTiles
 - d3d11_2/ID3D11DeviceContext2::UpdateTiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext2.UpdateTiles
---

# ID3D11DeviceContext2::UpdateTiles


## -description

Updates tiles by copying from app memory to the tiled resource.

## -parameters

### -param pDestTiledResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to a tiled resource to update.

### -param pDestTileRegionStartCoordinate [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate">D3D11_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the tiled resource.

### -param pDestTileRegionSize [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tile_region_size">D3D11_TILE_REGION_SIZE</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_tile_region_size">D3D11_TILE_REGION_SIZE</a> structure that describes the size of the tiled region.

### -param pSourceTileData [in]

Type: <b>const void*</b>

A pointer to memory that contains the source tile data that <b>UpdateTiles</b> uses to update the tiled resource.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_copy_flag">D3D11_TILE_COPY_FLAG</a>-typed values that are combined by using a bitwise OR operation. The only valid value is <b>D3D11_TILE_COPY_NO_OVERWRITE</b>.
 The other values aren't meaningful here, though
by definition the <b>D3D11_TILE_COPY_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE</b> value is basically what <b>UpdateTiles</b> does, but sources from app memory.

## -remarks

<b>UpdateTiles</b> drops write operations to unmapped areas (except on <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_tiled_resources_tier">Tier_1</a> tiled resources, where writing to unmapped areas is invalid).  

If a copy operation involves writing to the same memory location multiple times because multiple locations in the destination resource are mapped to the same tile memory, the resulting write operations to multi-mapped tiles are non-deterministic and non-repeatable; that is, accesses to the tile memory happen in whatever order the hardware happens to execute the copy operation.

The tiles involved in the copy operation can't include tiles that contain packed mipmaps or results of the copy operation are undefined. To transfer data to and from mipmaps that the hardware packs into one tile, you must use the standard (that is, non-tile specific) copy and update APIs (like <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1">ID3D11DeviceContext1::CopySubresourceRegion1</a> and <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1">ID3D11DeviceContext1::UpdateSubresource1</a>) or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips">ID3D11DeviceContext::GenerateMips</a> for the whole mipmap chain.

The memory layout of the data on the source side of the copy operation is linear in memory within 64 KB tiles, which the hardware and driver swizzle and deswizzle per tile as appropriate when they transfer to and from a tiled resource. For multisample antialiasing (MSAA) surfaces, the hardware and driver traverse each pixel's samples in sample-index order before they move to the next pixel. For tiles that are partially filled on the right side (for a surface that has a width not a multiple of tile width in pixels), the pitch and stride to move down a row is the full size in bytes of the number pixels that would fit across the tile if the tile was full. So, there can be a gap between each row of pixels in memory. Mipmaps that are smaller than a tile are not packed together in the linear layout, which might seem to be a waste of memory space, but as mentioned you can't use <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">ID3D11DeviceContext2::CopyTiles</a> or <b>UpdateTiles</b> to copy to mipmaps that the hardware packs together. You can just use generic copy and update APIs (like <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1">ID3D11DeviceContext1::CopySubresourceRegion1</a> and <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1">ID3D11DeviceContext1::UpdateSubresource1</a>) to copy small mipmaps individually. Although in the case of a generic copy API (like <b>ID3D11DeviceContext1::CopySubresourceRegion1</b>), the linear memory must be the same dimension as the tiled resource; <b>ID3D11DeviceContext1::CopySubresourceRegion1</b> can't copy from a buffer resource to a Texture2D for instance.

For more info about tiled resources, see <a href="/windows/desktop/direct3d11/tiled-resources">Tiled resources</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>