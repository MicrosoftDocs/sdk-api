---
UID: NS:d3d11_3.D3D11_TEX2D_ARRAY_RTV1
title: D3D11_TEX2D_ARRAY_RTV1
author: windows-driver-content
description: Describes the subresources from an array of 2D textures to use in a render-target view.
old-location: direct3d11\d3d11_tex2d_array_rtv1.htm
old-project: direct3d11
ms.assetid: AD1C80E6-B2C7-4110-B3C0-6A2B2063198B
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: D3D11_TEX2D_ARRAY_RTV1, D3D11_TEX2D_ARRAY_RTV1 structure [Direct3D 11], d3d11_3/D3D11_TEX2D_ARRAY_RTV1, direct3d11.d3d11_tex2d_array_rtv1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D11_TEX2D_ARRAY_RTV1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11_3.h
api_name:
-	D3D11_TEX2D_ARRAY_RTV1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

