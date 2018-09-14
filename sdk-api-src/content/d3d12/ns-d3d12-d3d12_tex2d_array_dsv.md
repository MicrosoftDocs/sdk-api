---
UID: NS:d3d12.D3D12_TEX2D_ARRAY_DSV
title: D3D12_TEX2D_ARRAY_DSV
author: windows-sdk-content
description: Describes the subresources from an array of 2D textures that are accessible to a depth-stencil view.
old-location: direct3d12\d3d12_tex2d_array_dsv.htm
tech.root: direct3d12
ms.assetid: 2B282647-8DCC-4624-8D35-0F63E0F93EE0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: D3D12_TEX2D_ARRAY_DSV, D3D12_TEX2D_ARRAY_DSV structure, d3d12/D3D12_TEX2D_ARRAY_DSV, direct3d12.d3d12_tex2d_array_dsv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D3D12_TEX2D_ARRAY_DSV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2D_ARRAY_DSV
req.redist: 
---

# D3D12_TEX2D_ARRAY_DSV structure


## -description


Describes the subresources from an array of 2D textures that are accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

The index of the first mipmap level to use.


### -field FirstArraySlice

The index of the first texture to use in an array of textures.


### -field ArraySize

Number of textures to use.


## -remarks



Use this structure with a <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure to view the resource as an array of 2D textures.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

