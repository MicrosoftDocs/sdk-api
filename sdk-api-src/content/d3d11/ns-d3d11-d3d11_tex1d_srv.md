---
UID: NS:d3d11.D3D11_TEX1D_SRV
title: D3D11_TEX1D_SRV (d3d11.h)
description: Specifies the subresource from a 1D texture to use in a shader-resource view. (D3D11_TEX1D_SRV)
helpviewer_keywords: ["1bcdba84-70d7-54b7-24fa-091adf73ae90","D3D11_TEX1D_SRV","D3D11_TEX1D_SRV structure [Direct3D 11]","d3d11/D3D11_TEX1D_SRV","direct3d11.d3d11_tex1d_srv"]
old-location: direct3d11\d3d11_tex1d_srv.htm
tech.root: direct3d11
ms.assetid: 255e97ac-e978-4a70-a908-f4537337dfeb
ms.date: 12/05/2018
ms.keywords: 1bcdba84-70d7-54b7-24fa-091adf73ae90, D3D11_TEX1D_SRV, D3D11_TEX1D_SRV structure [Direct3D 11], d3d11/D3D11_TEX1D_SRV, direct3d11.d3d11_tex1d_srv
req.header: d3d11.h
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
req.typenames: D3D11_TEX1D_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX1D_SRV
 - d3d11/D3D11_TEX1D_SRV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX1D_SRV
---

# D3D11_TEX1D_SRV structure


## -description

Specifies the subresource from a 1D texture to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture1D for which <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of mipmap levels for the view  of the texture. See the remarks.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

As an example, assuming <b>MostDetailedMip</b> = 6 and <b>MipLevels</b> = 2, the view will have access to 2 mipmap levels, 6 and 7, of the original texture for which <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> creates the view. In this situation, <b>MostDetailedMip</b> is greater than the <b>MipLevels</b> in the view. However, <b>MostDetailedMip</b> is not greater than the <b>MipLevels</b> in the original resource.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
