---
UID: NS:d3d12.D3D12_TEX1D_ARRAY_DSV
title: D3D12_TEX1D_ARRAY_DSV (d3d12.h)
description: Describes the subresources from an array of 1D textures to use in a depth-stencil view.
helpviewer_keywords: ["D3D12_TEX1D_ARRAY_DSV","D3D12_TEX1D_ARRAY_DSV structure","d3d12/D3D12_TEX1D_ARRAY_DSV","direct3d12.d3d12_tex1d_array_dsv"]
old-location: direct3d12\d3d12_tex1d_array_dsv.htm
tech.root: direct3d12
ms.assetid: 476937C8-D326-4DE4-8532-187AD0E2AFBB
ms.date: 12/05/2018
ms.keywords: D3D12_TEX1D_ARRAY_DSV, D3D12_TEX1D_ARRAY_DSV structure, d3d12/D3D12_TEX1D_ARRAY_DSV, direct3d12.d3d12_tex1d_array_dsv
req.header: d3d12.h
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
req.typenames: D3D12_TEX1D_ARRAY_DSV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX1D_ARRAY_DSV
 - d3d12/D3D12_TEX1D_ARRAY_DSV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEX1D_ARRAY_DSV
---

# D3D12_TEX1D_ARRAY_DSV structure


## -description

Describes the subresources from an array of 1D textures to use in a depth-stencil view.

## -struct-fields

### -field MipSlice

The index of the first mipmap level to use.

### -field FirstArraySlice

The index of the first texture to use in an array of textures.

### -field ArraySize

Number of textures to use.

## -remarks

Use this structure with a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure to view the resource as an array of 1D textures.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>