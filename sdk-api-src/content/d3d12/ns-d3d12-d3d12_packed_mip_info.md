---
UID: NS:d3d12.D3D12_PACKED_MIP_INFO
title: D3D12_PACKED_MIP_INFO (d3d12.h)
description: Describes the tile structure of a tiled resource with mipmaps. (D3D12_PACKED_MIP_INFO)
helpviewer_keywords: ["D3D12_PACKED_MIP_INFO","D3D12_PACKED_MIP_INFO structure","d3d12/D3D12_PACKED_MIP_INFO","direct3d12.d3d12_packed_mip_info"]
old-location: direct3d12\d3d12_packed_mip_info.htm
tech.root: direct3d12
ms.assetid: B9231C70-A6FF-4660-90B8-04207D2FF762
ms.date: 12/05/2018
ms.keywords: D3D12_PACKED_MIP_INFO, D3D12_PACKED_MIP_INFO structure, d3d12/D3D12_PACKED_MIP_INFO, direct3d12.d3d12_packed_mip_info
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
req.typenames: D3D12_PACKED_MIP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_PACKED_MIP_INFO
 - d3d12/D3D12_PACKED_MIP_INFO
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
 - D3D12_PACKED_MIP_INFO
---

# D3D12_PACKED_MIP_INFO structure


## -description

Describes the tile structure of a tiled resource with mipmaps.

## -struct-fields

### -field NumStandardMips

The number of standard mipmaps in the tiled resource.

### -field NumPackedMips

The number of packed mipmaps in the tiled resource.
          

This number starts from the least detailed mipmap (either sharing tiles or using non standard tile layout).
            This number is 0 if no such packing is in the resource.
            For array surfaces, this value is the number of mipmaps that are packed for a given array slice where each array slice repeats the same packing.
          

On Tier_2 tiled resources hardware, mipmaps that fill at least one standard shaped tile in all dimensions are not allowed to be included in the set of packed mipmaps.
            On Tier_1 hardware, mipmaps that are an integer multiple of one standard shaped tile in all dimensions are not allowed to be included in the set of packed mipmaps.
            Mipmaps with at least one dimension less than the standard tile shape may or may not be packed.
            When a given mipmap needs to be packed, all coarser mipmaps for a given array slice are considered packed as well.

### -field NumTilesForPackedMips

The number of tiles for the packed mipmaps in the tiled resource.
          

If there is no packing, this value is meaningless and is set to 0.
            Otherwise, it is set to the number of tiles that are needed to represent the set of packed mipmaps.
            The pixel layout within the packed mipmaps is hardware specific.
            If apps define only partial mappings for the set of tiles in packed mipmaps, read and write behavior is vendor specific and undefined.
            For arrays, this value is only the count of packed mipmaps within the subresources for each array slice.

### -field StartTileIndexInOverallResource

The offset of the first packed tile for the resource in the overall range of tiles.
            If <b>NumPackedMips</b> is 0, this value is meaningless and is 0.
            Otherwise, it is the offset of the first packed tile for the resource in the overall range of tiles for the resource.
            A value of 0 for <b>StartTileIndexInOverallResource</b> means the entire resource is packed.
            For array surfaces, this is the offset for the tiles that contain the packed mipmaps for the first array slice.
            Packed mipmaps for each array slice in arrayed surfaces are at this offset past the beginning of the tiles for each array slice.
            

<div class="alert"><b>Note</b>  The number of overall tiles, packed or not, for a given array slice is simply the total number of tiles for the resource divided by the resource's array size, 
              so it is easy to locate the range of tiles for any given array slice, out of which <b>StartTileIndexInOverallResource</b> identifies which of those are packed.
            </div>
<div> </div>

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling">GetResourceTiling</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-packed-mip-info">CD3DX12_PACKED_MIP_INFO</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
