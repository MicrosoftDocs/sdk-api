---
UID: NE:d3d11.D3D11_FILTER_TYPE
title: D3D11_FILTER_TYPE
author: windows-sdk-content
description: Types of magnification or minification sampler filters.
old-location: direct3d11\d3d11_filter_type.htm
tech.root: direct3d11
ms.assetid: 294ab4b3-a5fc-4b87-ae87-bf41752132b8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 63c13b99-0d2a-c3b3-f07f-5f244586124a, D3D11_FILTER_TYPE, D3D11_FILTER_TYPE enumeration [Direct3D 11], D3D11_FILTER_TYPE_LINEAR, D3D11_FILTER_TYPE_POINT, d3d11/D3D11_FILTER_TYPE, d3d11/D3D11_FILTER_TYPE_LINEAR, d3d11/D3D11_FILTER_TYPE_POINT, direct3d11.d3d11_filter_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D3D11_FILTER_TYPE
product: Windows
targetos: Windows
req.typenames: D3D11_FILTER_TYPE
req.redist: 
---

# D3D11_FILTER_TYPE enumeration


## -description


Types of magnification or minification sampler filters.


## -enum-fields




### -field D3D11_FILTER_TYPE_POINT

Point filtering used as a texture magnification or minification filter. The texel with coordinates nearest to the desired pixel value is used. The texture filter to be used between mipmap levels is nearest-point mipmap filtering. The rasterizer uses the color from the texel of the nearest mipmap texture. 


### -field D3D11_FILTER_TYPE_LINEAR

Bilinear interpolation filtering used as a texture magnification or minification filter. A weighted average of a 2 x 2 area of texels surrounding the desired pixel is used. The texture filter to use between mipmap levels is trilinear mipmap interpolation. The rasterizer linearly interpolates pixel color, using the texels of the two nearest mipmap textures. 


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

