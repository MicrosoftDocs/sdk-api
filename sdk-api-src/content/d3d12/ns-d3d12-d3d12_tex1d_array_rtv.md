---
UID: NS:d3d12.D3D12_TEX1D_ARRAY_RTV
title: D3D12_TEX1D_ARRAY_RTV (d3d12.h)
description: Describes the subresources from an array of 1D textures to use in a render-target view.
helpviewer_keywords: ["D3D12_TEX1D_ARRAY_RTV","D3D12_TEX1D_ARRAY_RTV structure","d3d12/D3D12_TEX1D_ARRAY_RTV","direct3d12.d3d12_tex1d_array_rtv"]
old-location: direct3d12\d3d12_tex1d_array_rtv.htm
tech.root: direct3d12
ms.assetid: AA297BF7-682B-4141-9F5B-D0C3B271C15A
ms.date: 12/05/2018
ms.keywords: D3D12_TEX1D_ARRAY_RTV, D3D12_TEX1D_ARRAY_RTV structure, d3d12/D3D12_TEX1D_ARRAY_RTV, direct3d12.d3d12_tex1d_array_rtv
f1_keywords:
- d3d12/D3D12_TEX1D_ARRAY_RTV
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D12.h
api_name:
- D3D12_TEX1D_ARRAY_RTV
targetos: Windows
req.typenames: D3D12_TEX1D_ARRAY_RTV
req.redist: 
ms.custom: 19H1
---

# D3D12_TEX1D_ARRAY_RTV structure


## -description


Describes the subresources from an array of 1D textures to use in a render-target view.


## -struct-fields




### -field MipSlice

The index of the mipmap level to use mip slice.


### -field FirstArraySlice

The index of the first texture to use in an array of textures.


### -field ArraySize

Number of textures to use.


## -remarks



Use this structure with a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc">D3D12_RENDER_TARGET_VIEW_DESC</a> structure to view the resource as an array of 1D textures.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

