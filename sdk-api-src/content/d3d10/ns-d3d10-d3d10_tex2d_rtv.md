---
UID: NS:d3d10.D3D10_TEX2D_RTV
title: D3D10_TEX2D_RTV (d3d10.h)
description: Specifies the subresource from a 2D texture to use in a render-target view. (D3D10_TEX2D_RTV)
helpviewer_keywords: ["21f542e7-4e2f-9c36-ae64-12c0d23732a8","D3D10_TEX2D_RTV","D3D10_TEX2D_RTV structure [Direct3D 10]","d3d10/D3D10_TEX2D_RTV","direct3d10.d3d10_tex2d_rtv"]
old-location: direct3d10\d3d10_tex2d_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2d_rtv.htm
ms.date: 12/05/2018
ms.keywords: 21f542e7-4e2f-9c36-ae64-12c0d23732a8, D3D10_TEX2D_RTV, D3D10_TEX2D_RTV structure [Direct3D 10], d3d10/D3D10_TEX2D_RTV, direct3d10.d3d10_tex2d_rtv
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
req.typenames: D3D10_TEX2D_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX2D_RTV
 - d3d10/D3D10_TEX2D_RTV
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
 - D3D10_TEX2D_RTV
---

# D3D10_TEX2D_RTV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a> to use in a render-target view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">mip slice</a>).

## -remarks

This structure is one member of a render-target-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
