---
UID: NE:d3d12.D3D12_FILTER_TYPE
title: D3D12_FILTER_TYPE
author: windows-sdk-content
description: Specifies the type of magnification or minification sampler filters.
old-location: direct3d12\d3d12_filter_type.htm
tech.root: direct3d12
ms.assetid: 3988D194-97C7-46C7-829D-154891684D68
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_FILTER_TYPE, D3D12_FILTER_TYPE enumeration, D3D12_FILTER_TYPE_LINEAR, D3D12_FILTER_TYPE_POINT, d3d12/D3D12_FILTER_TYPE, d3d12/D3D12_FILTER_TYPE_LINEAR, d3d12/D3D12_FILTER_TYPE_POINT, direct3d12.d3d12_filter_type
ms.topic: enum
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
 - D3D12_FILTER_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_FILTER_TYPE
req.redist: 
---

# D3D12_FILTER_TYPE enumeration


## -description


Specifies the type of magnification or minification sampler filters.




## -enum-fields




### -field D3D12_FILTER_TYPE_POINT

Point filtering is used as a texture magnification or minification filter. The texel with coordinates nearest to the desired pixel value is used. The texture filter to be used between mipmap levels is nearest-point mipmap filtering. The rasterizer uses the color from the texel of the nearest mipmap texture.


### -field D3D12_FILTER_TYPE_LINEAR

Bilinear interpolation filtering is used as a texture magnification or minification filter. A weighted average of a 2 x 2 area of texels surrounding the desired pixel is used. The texture filter to use between mipmap levels is trilinear mipmap interpolation. The rasterizer linearly interpolates pixel color, using the texels of the two nearest mipmap textures. 




## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a> structure. Also, refer to the remarks for <a href="https://msdn.microsoft.com/3755A722-34E5-415E-8760-93094D033E05">D3D12_FILTER</a>.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

