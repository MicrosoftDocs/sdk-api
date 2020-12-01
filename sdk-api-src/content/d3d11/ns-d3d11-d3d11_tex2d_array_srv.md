---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_SRV
title: D3D11_TEX2D_ARRAY_SRV (d3d11.h)
description: Specifies the subresources from an array of 2D textures to use in a shader-resource view.
helpviewer_keywords: ["45a6c17b-f09f-34db-329d-6ede8a9e8073","D3D11_TEX2D_ARRAY_SRV","D3D11_TEX2D_ARRAY_SRV structure [Direct3D 11]","d3d11/D3D11_TEX2D_ARRAY_SRV","direct3d11.d3d11_tex2d_array_srv"]
old-location: direct3d11\d3d11_tex2d_array_srv.htm
tech.root: direct3d11
ms.assetid: 274e7a15-ac54-41e2-87d7-484e3e768a38
ms.date: 12/05/2018
ms.keywords: 45a6c17b-f09f-34db-329d-6ede8a9e8073, D3D11_TEX2D_ARRAY_SRV, D3D11_TEX2D_ARRAY_SRV structure [Direct3D 11], d3d11/D3D11_TEX2D_ARRAY_SRV, direct3d11.d3d11_tex2d_array_srv
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
req.typenames: D3D11_TEX2D_ARRAY_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_ARRAY_SRV
 - d3d11/D3D11_TEX2D_ARRAY_SRV
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
 - D3D11_TEX2D_ARRAY_SRV
---

# D3D11_TEX2D_ARRAY_SRV structure


## -description

Specifies the subresources from an array of 2D textures to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture2D for which <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.

### -field FirstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures.

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures in the array.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>