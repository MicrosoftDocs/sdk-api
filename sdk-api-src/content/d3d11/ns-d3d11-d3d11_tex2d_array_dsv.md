---
UID: NS:d3d11.D3D11_TEX2D_ARRAY_DSV
title: D3D11_TEX2D_ARRAY_DSV
author: windows-sdk-content
description: Specifies the subresources from an array 2D textures that are accessible to a depth-stencil view.
old-location: direct3d11\d3d11_tex2d_array_dsv.htm
tech.root: direct3d11
ms.assetid: 0cf77ebd-a83c-4021-866d-664913549d80
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2ebbfb28-3f63-3075-24ab-73fe477fd606, D3D11_TEX2D_ARRAY_DSV, D3D11_TEX2D_ARRAY_DSV structure [Direct3D 11], d3d11/D3D11_TEX2D_ARRAY_DSV, direct3d11.d3d11_tex2d_array_dsv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D3D11_TEX2D_ARRAY_DSV
product: Windows
targetos: Windows
req.typenames: D3D11_TEX2D_ARRAY_DSV
req.redist: 
---

# D3D11_TEX2D_ARRAY_DSV structure


## -description


Specifies the subresources from an array 2D textures that are accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first mipmap level to use.


### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures.


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a depth-stencil-view description (see <a href="https://msdn.microsoft.com/f073a798-edd5-4e6a-a8a7-1592721ce35d">D3D11_DEPTH_STENCIL_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

