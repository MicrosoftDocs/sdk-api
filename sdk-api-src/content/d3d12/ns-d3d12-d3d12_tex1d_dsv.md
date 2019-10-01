---
UID: NS:d3d12.D3D12_TEX1D_DSV
title: D3D12_TEX1D_DSV (d3d12.h)
author: windows-sdk-content
description: Describes the subresource from a 1D texture that is accessible to a depth-stencil view.
old-location: direct3d12\d3d12_tex1d_dsv.htm
tech.root: direct3d12
ms.assetid: 42136891-8D7B-40CC-B683-77549BE8DE3C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_TEX1D_DSV, D3D12_TEX1D_DSV structure, d3d12/D3D12_TEX1D_DSV, direct3d12.d3d12_tex1d_dsv
ms.topic: struct
f1_keywords: 
 - "d3d12/D3D12_TEX1D_DSV"
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
 - D3D12_TEX1D_DSV
targetos: Windows
req.typenames: D3D12_TEX1D_DSV
req.redist: 
ms.custom: 19H1
---

# D3D12_TEX1D_DSV structure


## -description


Describes the subresource from a 1D texture that is accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

The index of the first mipmap level to use.


## -remarks



Use this structure with a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure to view the resource as a 1D texture.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

