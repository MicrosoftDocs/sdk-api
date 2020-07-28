---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_RTV
title: D3D11_TEX2D_ARRAY_RTV (d3d11.h)
description: Specifies the subresources from an array of 2D textures to use in a render-target view.
helpviewer_keywords: ["46c5645a-0f21-8bfe-b2e9-ab115657b0c0","D3D11_TEX2D_ARRAY_RTV","D3D11_TEX2D_ARRAY_RTV structure [Direct3D 11]","d3d11/D3D11_TEX2D_ARRAY_RTV","direct3d11.d3d11_tex2d_array_rtv"]
old-location: direct3d11\d3d11_tex2d_array_rtv.htm
tech.root: direct3d11
ms.assetid: 5caecf26-707b-45f4-8296-784ed4184459
ms.date: 12/05/2018
ms.keywords: 46c5645a-0f21-8bfe-b2e9-ab115657b0c0, D3D11_TEX2D_ARRAY_RTV, D3D11_TEX2D_ARRAY_RTV structure [Direct3D 11], d3d11/D3D11_TEX2D_ARRAY_RTV, direct3d11.d3d11_tex2d_array_rtv
f1_keywords:
- d3d11/D3D11_TEX2D_ARRAY_RTV
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D11.h
api_name:
- D3D11_TEX2D_ARRAY_RTV
targetos: Windows
req.typenames: D3D11_TEX2D_ARRAY_RTV
req.redist: 
ms.custom: 19H1
---

# D3D11_TEX2D_ARRAY_RTV structure


## -description


Specifies the subresources from an array of 2D textures to use in a render-target view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the mipmap level to use mip slice.


### -field FirstArraySlice

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures.


### -field ArraySize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures in the array to use in the render target view, starting from <b>FirstArraySlice</b>.


## -remarks



This structure is one member of a render-target-view description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_render_target_view_desc">D3D11_RENDER_TARGET_VIEW_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
 

 

