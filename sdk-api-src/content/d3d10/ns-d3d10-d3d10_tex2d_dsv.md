---
UID: NS:d3d10.D3D10_TEX2D_DSV
title: D3D10_TEX2D_DSV (d3d10.h)
description: Specifies the subresource from a 2D texture that is accessible to a depth-stencil view. (D3D10_TEX2D_DSV)
helpviewer_keywords: ["D3D10_TEX2D_DSV","D3D10_TEX2D_DSV structure [Direct3D 10]","c7842b23-969e-3b59-100f-750283b6b232","d3d10/D3D10_TEX2D_DSV","direct3d10.d3d10_tex2d_dsv"]
old-location: direct3d10\d3d10_tex2d_dsv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2d_dsv.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEX2D_DSV, D3D10_TEX2D_DSV structure [Direct3D 10], c7842b23-969e-3b59-100f-750283b6b232, d3d10/D3D10_TEX2D_DSV, direct3d10.d3d10_tex2d_dsv
req.header: d3d10.h
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
req.typenames: D3D10_TEX2D_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX2D_DSV
 - d3d10/D3D10_TEX2D_DSV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEX2D_DSV
---

# D3D10_TEX2D_DSV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a> that is accessible to a depth-stencil view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first mipmap level to use (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">mip slice</a>).

## -remarks

This structure is one member of a depth-stencil-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_view_desc">D3D10_DEPTH_STENCIL_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
