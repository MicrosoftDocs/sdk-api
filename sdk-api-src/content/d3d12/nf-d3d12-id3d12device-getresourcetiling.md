---
UID: NF:d3d12.ID3D12Device.GetResourceTiling
title: ID3D12Device::GetResourceTiling
author: windows-sdk-content
description: Gets info about how a tiled resource is broken into tiles.
old-location: direct3d12\id3d12device_getresourcetiling.htm
tech.root: direct3d12
ms.assetid: 32574750-92D3-4CAF-90C6-BA0DEF1E5464
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetResourceTiling, GetResourceTiling method, GetResourceTiling method,ID3D12Device interface, ID3D12Device interface,GetResourceTiling method, ID3D12Device.GetResourceTiling, ID3D12Device::GetResourceTiling, d3d12/ID3D12Device::GetResourceTiling, direct3d12.id3d12device_getresourcetiling
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device.GetResourceTiling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12Device.GetResourceTiling
: 
---

# ID3D12Device::GetResourceTiling


## -description


Gets info about how a tiled resource is broken into tiles.
        


## -parameters




### -param pTiledResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>*</b>

Specifies a tiled <a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>  to get info about.
          


### -param pNumTilesForEntireResource [out, optional]

Type: <b>UINT*</b>

A pointer to a variable that receives the number of tiles needed to store the entire tiled resource.
          


### -param pPackedMipDesc [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn986736(v=VS.85).aspx">D3D12_PACKED_MIP_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn986736(v=VS.85).aspx">D3D12_PACKED_MIP_INFO</a> structure that <b>GetResourceTiling</b> fills with info about how the tiled resource's mipmaps are packed.
          


### -param pStandardTileShapeForNonPackedMips [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn770449(v=VS.85).aspx">D3D12_TILE_SHAPE</a>*</b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Dn770449(v=VS.85).aspx">D3D12_TILE_SHAPE</a> structure that <b>GetResourceTiling</b> fills with info about the tile shape. This is info about how pixels fit in the tiles, independent of tiled resource's dimensions, not including packed mipmaps. If the entire tiled resource is packed, this parameter is meaningless because the tiled resource has no defined layout for packed mipmaps. In this situation, <b>GetResourceTiling</b> sets the members of D3D12_TILE_SHAPE to zeros.
          


### -param pNumSubresourceTilings [in, out, optional]

Type: <b>UINT*</b>

A pointer to a variable that contains the number of tiles in the subresource. On input, this is the number of subresources to query tilings for; on output, this is the number that was actually retrieved at <i>pSubresourceTilingsForNonPackedMips</i> (clamped to what's available).
          


### -param FirstSubresourceTilingToGet [in]

Type: <b>UINT</b>

The number of the first subresource tile to get. <b>GetResourceTiling</b> ignores this parameter if the number that <i>pNumSubresourceTilings</i> points to is 0.
          


### -param pSubresourceTilingsForNonPackedMips [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn770412(v=VS.85).aspx">D3D12_SUBRESOURCE_TILING</a>*</b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Dn770412(v=VS.85).aspx">D3D12_SUBRESOURCE_TILING</a> structure that <b>GetResourceTiling</b> fills with info about subresource tiles. If subresource tiles are part of packed mipmaps, <b>GetResourceTiling</b> sets the members of D3D12_SUBRESOURCE_TILING to zeros, except the <i>StartTileIndexInOverallResource</i> member, which <b>GetResourceTiling</b> sets to D3D12_PACKED_TILE (0xffffffff). The D3D12_PACKED_TILE constant indicates that the whole <b>D3D12_SUBRESOURCE_TILING</b> structure is meaningless for this situation, and the info that the <i>pPackedMipDesc</i> parameter points to applies.
          


## -returns



This method does not return a value.
          




## -remarks



To estimate the total resource size of textures needed when calculating heap sizes and calling <a href="https://msdn.microsoft.com/en-us/library/Dn899180(v=VS.85).aspx">CreatePlacedResource</a>, use <a href="https://msdn.microsoft.com/en-us/library/Dn788680(v=VS.85).aspx">GetResourceAllocationInfo</a> instead of <b>GetResourceTiling</b>.
          <b>GetResourceTiling</b> cannot be used for this.
        

For more information on tiled resources, refer to <a href="https://msdn.microsoft.com/en-us/library/Dn903951(v=VS.85).aspx">Volume Tiled Resources</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn705766(v=VS.85).aspx">Subresources</a>
 

 

