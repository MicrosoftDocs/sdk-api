---
UID: NS:d3d11.D3D11_TEX3D_RTV
title: D3D11_TEX3D_RTV (d3d11.h)
description: Specifies the subresources from a 3D texture to use in a render-target view.
helpviewer_keywords: ["0e151840-ecbe-6a4e-52dd-154d488710bc","D3D11_TEX3D_RTV","D3D11_TEX3D_RTV structure [Direct3D 11]","d3d11/D3D11_TEX3D_RTV","direct3d11.d3d11_tex3d_rtv"]
old-location: direct3d11\d3d11_tex3d_rtv.htm
tech.root: direct3d11
ms.assetid: 58a4b383-ad5d-4eb0-bff5-8825c3ae8dd1
ms.date: 12/05/2018
ms.keywords: 0e151840-ecbe-6a4e-52dd-154d488710bc, D3D11_TEX3D_RTV, D3D11_TEX3D_RTV structure [Direct3D 11], d3d11/D3D11_TEX3D_RTV, direct3d11.d3d11_tex3d_rtv
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
req.typenames: D3D11_TEX3D_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX3D_RTV
 - d3d11/D3D11_TEX3D_RTV
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
 - D3D11_TEX3D_RTV
---

# D3D11_TEX3D_RTV structure


## -description

Specifies the subresources from a 3D texture to use in a render-target view.

## -struct-fields

### -field MipSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use mip slice.

### -field FirstWSlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

First depth level to use.

### -field WSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of depth levels to use in the render-target view, starting from <b>FirstWSlice</b>. A value of -1 indicates all of the slices along the w axis, starting from <b>FirstWSlice</b>.

## -remarks

This structure is one member of a render target view. See <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_render_target_view_desc">D3D11_RENDER_TARGET_VIEW_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>