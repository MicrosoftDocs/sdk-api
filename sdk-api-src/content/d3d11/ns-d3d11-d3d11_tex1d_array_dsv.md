---
UID: NS:d3d11.D3D11_TEX1D_ARRAY_DSV
title: D3D11_TEX1D_ARRAY_DSV (d3d11.h)
description: Specifies the subresources from an array of 1D textures to use in a depth-stencil view.
helpviewer_keywords: ["79a5c13b-e6bb-ddae-ebd4-aa756cc5a746","D3D11_TEX1D_ARRAY_DSV","D3D11_TEX1D_ARRAY_DSV structure [Direct3D 11]","d3d11/D3D11_TEX1D_ARRAY_DSV","direct3d11.d3d11_tex1d_array_dsv"]
old-location: direct3d11\d3d11_tex1d_array_dsv.htm
tech.root: direct3d11
ms.assetid: 9e4233cc-680a-486e-b91a-732d055937d1
ms.date: 12/05/2018
ms.keywords: 79a5c13b-e6bb-ddae-ebd4-aa756cc5a746, D3D11_TEX1D_ARRAY_DSV, D3D11_TEX1D_ARRAY_DSV structure [Direct3D 11], d3d11/D3D11_TEX1D_ARRAY_DSV, direct3d11.d3d11_tex1d_array_dsv
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
req.typenames: D3D11_TEX1D_ARRAY_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX1D_ARRAY_DSV
 - d3d11/D3D11_TEX1D_ARRAY_DSV
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
 - D3D11_TEX1D_ARRAY_DSV
---

# D3D11_TEX1D_ARRAY_DSV structure


## -description

Specifies the subresources from an array of 1D textures to use in a depth-stencil view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first mipmap level to use.

### -field FirstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures.

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures to use.

## -remarks

This structure is one member of a depth-stencil-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>