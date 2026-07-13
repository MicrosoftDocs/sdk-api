---
UID: NS:d3d11_3.D3D11_TEX2D_ARRAY_RTV1
title: D3D11_TEX2D_ARRAY_RTV1 (d3d11_3.h)
description: Describes the subresources from an array of 2D textures to use in a render-target view. (D3D11_TEX2D_ARRAY_RTV1)
helpviewer_keywords: ["D3D11_TEX2D_ARRAY_RTV1","D3D11_TEX2D_ARRAY_RTV1 structure [Direct3D 11]","d3d11_3/D3D11_TEX2D_ARRAY_RTV1","direct3d11.d3d11_tex2d_array_rtv1"]
old-location: direct3d11\d3d11_tex2d_array_rtv1.htm
tech.root: direct3d11
ms.assetid: AD1C80E6-B2C7-4110-B3C0-6A2B2063198B
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2D_ARRAY_RTV1, D3D11_TEX2D_ARRAY_RTV1 structure [Direct3D 11], d3d11_3/D3D11_TEX2D_ARRAY_RTV1, direct3d11.d3d11_tex2d_array_rtv1
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
req.typenames: D3D11_TEX2D_ARRAY_RTV1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_ARRAY_RTV1
 - d3d11_3/D3D11_TEX2D_ARRAY_RTV1
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
 - D3D11_TEX2D_ARRAY_RTV1
---

# D3D11_TEX2D_ARRAY_RTV1 structure


## -description

Describes the subresources from an array of 2D textures to use in a render-target view.

## -struct-fields

### -field MipSlice

The index of the mipmap level to use mip slice.

### -field FirstArraySlice

The index of the first texture to use in an array of textures.

### -field ArraySize

Number of textures in the array to use in the render-target view, starting from <b>FirstArraySlice</b>.

### -field PlaneSlice

The index (plane slice number) of the plane to use in an array of textures.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
