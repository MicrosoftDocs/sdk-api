---
UID: NS:d3d10.D3D10_TEX3D_RTV
title: D3D10_TEX3D_RTV (d3d10.h)
description: Specifies the subresource(s) from a 3D texture to use in a render-target view.
helpviewer_keywords: ["D3D10_TEX3D_RTV","D3D10_TEX3D_RTV structure [Direct3D 10]","a846ce63-d213-1889-2297-8bc813006637","d3d10/D3D10_TEX3D_RTV","direct3d10.d3d10_tex3d_rtv"]
old-location: direct3d10\d3d10_tex3d_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex3d_rtv.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEX3D_RTV, D3D10_TEX3D_RTV structure [Direct3D 10], a846ce63-d213-1889-2297-8bc813006637, d3d10/D3D10_TEX3D_RTV, direct3d10.d3d10_tex3d_rtv
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
req.typenames: D3D10_TEX3D_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX3D_RTV
 - d3d10/D3D10_TEX3D_RTV
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
 - D3D10_TEX3D_RTV
---

# D3D10_TEX3D_RTV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource(s)</a> from a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">3D texture</a> to use in a render-target view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">mip slice</a>).

### -field FirstWSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

First depth level to use.

### -field WSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of depth levels to use in the render-target view, starting from <b>FirstWSlice</b>. A value of -1 indicates all of the slices along the w axis, starting from <b>FirstWSlice</b>.

## -remarks

This structure is one member of a render target view. See <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>