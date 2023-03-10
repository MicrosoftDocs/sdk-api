---
UID: NS:d3d11.D3D11_TEX3D_SRV
title: D3D11_TEX3D_SRV (d3d11.h)
description: Specifies the subresources from a 3D texture to use in a shader-resource view.
helpviewer_keywords: ["6aca102c-9b7d-44ab-5f28-da578e24ba0c","D3D11_TEX3D_SRV","D3D11_TEX3D_SRV structure [Direct3D 11]","d3d11/D3D11_TEX3D_SRV","direct3d11.d3d11_tex3d_srv"]
old-location: direct3d11\d3d11_tex3d_srv.htm
tech.root: direct3d11
ms.assetid: d6aacaa5-5314-4ea1-b12e-0ffba850e74c
ms.date: 12/05/2018
ms.keywords: 6aca102c-9b7d-44ab-5f28-da578e24ba0c, D3D11_TEX3D_SRV, D3D11_TEX3D_SRV structure [Direct3D 11], d3d11/D3D11_TEX3D_SRV, direct3d11.d3d11_tex3d_srv
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
req.typenames: D3D11_TEX3D_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX3D_SRV
 - d3d11/D3D11_TEX3D_SRV
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
 - D3D11_TEX3D_SRV
---

# D3D11_TEX3D_SRV structure


## -description

Specifies the subresources from a 3D texture to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> (from the original Texture3D for which <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a> creates a view) -1.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>.

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>