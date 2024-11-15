---
UID: NF:d3d12.ID3D12Device.GetResourceTiling
title: ID3D12Device::GetResourceTiling (d3d12.h)
description: Gets info about how a tiled resource is broken into tiles. (ID3D12Device.GetResourceTiling)
helpviewer_keywords: ["GetResourceTiling","GetResourceTiling method","GetResourceTiling method","ID3D12Device interface","ID3D12Device interface","GetResourceTiling method","ID3D12Device.GetResourceTiling","ID3D12Device::GetResourceTiling","d3d12/ID3D12Device::GetResourceTiling","direct3d12.id3d12device_getresourcetiling"]
old-location: direct3d12\id3d12device_getresourcetiling.htm
tech.root: direct3d12
ms.assetid: 32574750-92D3-4CAF-90C6-BA0DEF1E5464
ms.date: 12/05/2018
ms.keywords: GetResourceTiling, GetResourceTiling method, GetResourceTiling method,ID3D12Device interface, ID3D12Device interface,GetResourceTiling method, ID3D12Device.GetResourceTiling, ID3D12Device::GetResourceTiling, d3d12/ID3D12Device::GetResourceTiling, direct3d12.id3d12device_getresourcetiling
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
 - ID3D12Device::GetResourceTiling
 - d3d12/ID3D12Device::GetResourceTiling
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
 - ID3D12Device.GetResourceTiling
---

# ID3D12Device::GetResourceTiling


## -description

Gets info about how a tiled resource is broken into tiles.

## -parameters

### -param pTiledResource [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

Specifies a tiled <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>  to get info about.

### -param pNumTilesForEntireResource [out, optional]

Type: <b>UINT*</b>

A pointer to a variable that receives the number of tiles needed to store the entire tiled resource.

### -param pPackedMipDesc [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info">D3D12_PACKED_MIP_INFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info">D3D12_PACKED_MIP_INFO</a> structure that <b>GetResourceTiling</b> fills with info about how the tiled resource's mipmaps are packed.

### -param pStandardTileShapeForNonPackedMips [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape">D3D12_TILE_SHAPE</a>*</b>

Specifies a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape">D3D12_TILE_SHAPE</a> structure that <b>GetResourceTiling</b> fills with info about the tile shape. This is info about how pixels fit in the tiles, independent of tiled resource's dimensions, not including packed mipmaps. If the entire tiled resource is packed, this parameter is meaningless because the tiled resource has no defined layout for packed mipmaps. In this situation, <b>GetResourceTiling</b> sets the members of D3D12_TILE_SHAPE to zeros.

### -param pNumSubresourceTilings [in, out, optional]

Type: <b>UINT*</b>

A pointer to a variable that contains the number of tiles in the subresource. On input, this is the number of subresources to query tilings for; on output, this is the number that was actually retrieved at <i>pSubresourceTilingsForNonPackedMips</i> (clamped to what's available).

### -param FirstSubresourceTilingToGet [in]

Type: <b>UINT</b>

The number of the first subresource tile to get. <b>GetResourceTiling</b> ignores this parameter if the number that <i>pNumSubresourceTilings</i> points to is 0.

### -param pSubresourceTilingsForNonPackedMips [out]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling">D3D12_SUBRESOURCE_TILING</a>*</b>

Specifies a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling">D3D12_SUBRESOURCE_TILING</a> structure that <b>GetResourceTiling</b> fills with info about subresource tiles. If subresource tiles are part of packed mipmaps, <b>GetResourceTiling</b> sets the members of D3D12_SUBRESOURCE_TILING to zeros, except the <i>StartTileIndexInOverallResource</i> member, which <b>GetResourceTiling</b> sets to D3D12_PACKED_TILE (0xffffffff). The D3D12_PACKED_TILE constant indicates that the whole <b>D3D12_SUBRESOURCE_TILING</b> structure is meaningless for this situation, and the info that the <i>pPackedMipDesc</i> parameter points to applies.

## -remarks

To estimate the total resource size of textures needed when calculating heap sizes and calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>, use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo(uint_uint_constd3d12_resource_desc)">GetResourceAllocationInfo</a> instead of <b>GetResourceTiling</b>.
          <b>GetResourceTiling</b> cannot be used for this.
        

For more information on tiled resources, refer to <a href="/windows/desktop/direct3d12/volume-tiled-resources">Volume Tiled Resources</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/desktop/direct3d12/subresources">Subresources</a>
