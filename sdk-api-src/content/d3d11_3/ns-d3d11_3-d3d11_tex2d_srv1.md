---
UID: NS:d3d11_3.D3D11_TEX2D_SRV1
title: D3D11_TEX2D_SRV1 (d3d11_3.h)
description: Describes the subresource from a 2D texture to use in a shader-resource view. (D3D11_TEX2D_SRV1)
helpviewer_keywords: ["D3D11_TEX2D_SRV1","D3D11_TEX2D_SRV1 structure [Direct3D 11]","d3d11_3/D3D11_TEX2D_SRV1","direct3d11.d3d11_tex2d_srv1"]
old-location: direct3d11\d3d11_tex2d_srv1.htm
tech.root: direct3d11
ms.assetid: 5C5D8BF8-1B3E-4FEF-ACD7-FCEAEE335DFE
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2D_SRV1, D3D11_TEX2D_SRV1 structure [Direct3D 11], d3d11_3/D3D11_TEX2D_SRV1, direct3d11.d3d11_tex2d_srv1
req.header: d3d11_3.h
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
req.typenames: D3D11_TEX2D_SRV1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_SRV1
 - d3d11_3/D3D11_TEX2D_SRV1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_TEX2D_SRV1
---

# D3D11_TEX2D_SRV1 structure


## -description

Describes the subresource from a 2D texture to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Index of the most detailed mipmap level to use; this number is between 0 and (<b>MipLevels</b> (from the original Texture2D for which 
            <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createshaderresourceview1">ID3D11Device3::CreateShaderResourceView1</a> creates a view) - 1 ).

### -field MipLevels

The maximum number of mipmap levels for the view of the texture. See the remarks in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_tex1d_srv">D3D11_TEX1D_SRV</a>.
            

Set to -1 to indicate all the mipmap levels from <b>MostDetailedMip</b> on down to least detailed.

### -field PlaneSlice

The index (plane slice number) of the plane to use in the texture.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
