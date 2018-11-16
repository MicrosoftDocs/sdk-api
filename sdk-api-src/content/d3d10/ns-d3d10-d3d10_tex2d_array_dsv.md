---
UID: NS:d3d10.D3D10_TEX2D_ARRAY_DSV
title: D3D10_TEX2D_ARRAY_DSV
author: windows-sdk-content
description: Specifies the subresource(s) from an array 2D textures that are accessible to a depth-stencil view.
old-location: direct3d10\d3d10_tex2d_array_dsv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2d_array_dsv.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D10_TEX2D_ARRAY_DSV, D3D10_TEX2D_ARRAY_DSV structure [Direct3D 10], b74f90e0-46e3-78ef-850f-dc574308fe4b, d3d10/D3D10_TEX2D_ARRAY_DSV, direct3d10.d3d10_tex2d_array_dsv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10.h
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
 - D3D10.h
api_name:
 - D3D10_TEX2D_ARRAY_DSV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX2D_ARRAY_DSV
req.redist: 
---

# D3D10_TEX2D_ARRAY_DSV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from an array <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D textures</a> that are accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first mipmap level to use (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">mip slice</a>).


### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">array slice</a>)


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a depth-stencil-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205037(v=VS.85).aspx">D3D10_DEPTH_STENCIL_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

