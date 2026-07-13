---
UID: NS:d3d11.D3D11_TEX2D_DSV
title: D3D11_TEX2D_DSV (d3d11.h)
description: Specifies the subresource from a 2D texture that is accessible to a depth-stencil view. (D3D11_TEX2D_DSV)
helpviewer_keywords: ["3ffa1de6-be1c-8657-b069-f9b2e05cbbe8","D3D11_TEX2D_DSV","D3D11_TEX2D_DSV structure [Direct3D 11]","d3d11/D3D11_TEX2D_DSV","direct3d11.d3d11_tex2d_dsv"]
old-location: direct3d11\d3d11_tex2d_dsv.htm
tech.root: direct3d11
ms.assetid: f3f7aeca-e6c1-445c-97f4-1968b726dad7
ms.date: 12/05/2018
ms.keywords: 3ffa1de6-be1c-8657-b069-f9b2e05cbbe8, D3D11_TEX2D_DSV, D3D11_TEX2D_DSV structure [Direct3D 11], d3d11/D3D11_TEX2D_DSV, direct3d11.d3d11_tex2d_dsv
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
req.typenames: D3D11_TEX2D_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_DSV
 - d3d11/D3D11_TEX2D_DSV
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
 - D3D11_TEX2D_DSV
---

# D3D11_TEX2D_DSV structure


## -description

Specifies the subresource from a 2D texture that is accessible to a depth-stencil view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first mipmap level to use.

## -remarks

This structure is one member of a depth-stencil-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
