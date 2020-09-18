---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_DSV
title: D3D11_TEX2D_ARRAY_DSV (d3d11.h)
description: Specifies the subresources from an array 2D textures that are accessible to a depth-stencil view.
helpviewer_keywords: ["2ebbfb28-3f63-3075-24ab-73fe477fd606","D3D11_TEX2D_ARRAY_DSV","D3D11_TEX2D_ARRAY_DSV structure [Direct3D 11]","d3d11/D3D11_TEX2D_ARRAY_DSV","direct3d11.d3d11_tex2d_array_dsv"]
old-location: direct3d11\d3d11_tex2d_array_dsv.htm
tech.root: direct3d11
ms.assetid: 0cf77ebd-a83c-4021-866d-664913549d80
ms.date: 12/05/2018
ms.keywords: 2ebbfb28-3f63-3075-24ab-73fe477fd606, D3D11_TEX2D_ARRAY_DSV, D3D11_TEX2D_ARRAY_DSV structure [Direct3D 11], d3d11/D3D11_TEX2D_ARRAY_DSV, direct3d11.d3d11_tex2d_array_dsv
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
req.typenames: D3D11_TEX2D_ARRAY_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_ARRAY_DSV
 - d3d11/D3D11_TEX2D_ARRAY_DSV
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
 - D3D11_TEX2D_ARRAY_DSV
---

# D3D11_TEX2D_ARRAY_DSV structure


## -description

Specifies the subresources from an array 2D textures that are accessible to a depth-stencil view.

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