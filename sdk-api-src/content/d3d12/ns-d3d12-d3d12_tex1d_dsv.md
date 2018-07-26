---
UID: NS:d3d12.D3D12_TEX1D_DSV
title: D3D12_TEX1D_DSV
author: windows-sdk-content
description: Describes the subresource from a 1D texture that is accessible to a depth-stencil view.
old-location: direct3d12\d3d12_tex1d_dsv.htm
old-project: direct3d12
ms.assetid: 42136891-8D7B-40CC-B683-77549BE8DE3C
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D12_TEX1D_DSV, D3D12_TEX1D_DSV structure, d3d12/D3D12_TEX1D_DSV, direct3d12.d3d12_tex1d_dsv
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
tech.root: 
req.typenames: D3D12_TEX1D_DSV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEX1D_DSV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_TEX1D_DSV structure


## -description


Describes the subresource from a 1D texture that is accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

The index of the first mipmap level to use.


## -remarks



Use this structure with a <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure to view the resource as a 1D texture.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

