---
UID: NF:d3d11_2.ID3D11Device2.GetResourceTiling
title: ID3D11Device2::GetResourceTiling
author: windows-sdk-content
description: Gets info about how a tiled resource is broken into tiles.
old-location: direct3d11\id3d11device2_getresourcetiling.htm
tech.root: direct3d11
ms.assetid: 51E7C948-5B14-4389-94BA-DB0DA7DFFC14
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetResourceTiling, GetResourceTiling method [Direct3D 11], GetResourceTiling method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],GetResourceTiling method, ID3D11Device2.GetResourceTiling, ID3D11Device2::GetResourceTiling, d3d11_2/ID3D11Device2::GetResourceTiling, direct3d11.id3d11device2_getresourcetiling
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device2.GetResourceTiling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device2::GetResourceTiling


## -description


Gets info about how a tiled resource is broken into tiles.


## -parameters




### -param pTiledResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the tiled resource to get info about.


### -param pNumTilesForEntireResource [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that receives the number of tiles needed to store the entire tiled resource. 


### -param pPackedMipDesc [out, optional]

Type: <b><a href="https://msdn.microsoft.com/1c200c44-6cd6-4e77-8187-54cd6cd79c84">D3D11_PACKED_MIP_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/1c200c44-6cd6-4e77-8187-54cd6cd79c84">D3D11_PACKED_MIP_DESC</a> structure that <b>GetResourceTiling</b> fills with info about how the tiled resource's mipmaps are packed.
          


### -param pStandardTileShapeForNonPackedMips [out, optional]

Type: <b><a href="https://msdn.microsoft.com/B4B9D82C-2890-4CC4-AB5C-026FBD931B4E">D3D11_TILE_SHAPE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/B4B9D82C-2890-4CC4-AB5C-026FBD931B4E">D3D11_TILE_SHAPE</a> structure that <b>GetResourceTiling</b> fills with info about the tile shape. This is info about how pixels fit in the tiles, independent of tiled resource's dimensions,
            not including packed mipmaps.  If the entire tiled resource is packed, this parameter is meaningless because the tiled resource has no defined layout
            for packed mipmaps.
            In this situation, <b>GetResourceTiling</b> sets the members of <b>D3D11_TILE_SHAPE</b> to zeros.
          


### -param pNumSubresourceTilings [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that contains the number of tiles in the subresource. On input, this is the number of subresources to query tilings for; on output, this is the number that was actually retrieved at <i>pSubresourceTilingsForNonPackedMips</i> (clamped to what's available).
          


### -param FirstSubresourceTilingToGet [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of the first subresource tile to get. <b>GetResourceTiling</b> ignores this parameter if the number that <i>pNumSubresourceTilings</i> points to is 0.
          


### -param pSubresourceTilingsForNonPackedMips [out]

Type: <b><a href="https://msdn.microsoft.com/679E4AD1-3AC8-4055-9D38-37776E2D17BE">D3D11_SUBRESOURCE_TILING</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/679E4AD1-3AC8-4055-9D38-37776E2D17BE">D3D11_SUBRESOURCE_TILING</a> structure that <b>GetResourceTiling</b> fills with info about subresource tiles.
          

If subresource tiles are part of packed mipmaps, <b>GetResourceTiling</b> sets the members of <a href="https://msdn.microsoft.com/679E4AD1-3AC8-4055-9D38-37776E2D17BE">D3D11_SUBRESOURCE_TILING</a> to zeros, except the <b>StartTileIndexInOverallResource</b> member, which <b>GetResourceTiling</b> sets to <b>D3D11_PACKED_TILE</b> (0xffffffff). The <b>D3D11_PACKED_TILE</b> constant indicates that the whole
            <b>D3D11_SUBRESOURCE_TILING</b> structure is meaningless for this situation, and the info that the <i>pPackedMipDesc</i> parameter points to applies.
          


## -returns



Returns nothing




## -remarks



For more info about tiled resources, see <a href="https://msdn.microsoft.com/03083460-192B-40CB-8EE1-76DF6D95F72B">Tiled resources</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>
 

 

