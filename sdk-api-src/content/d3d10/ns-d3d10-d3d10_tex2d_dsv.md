---
UID: NS:d3d10.D3D10_TEX2D_DSV
title: D3D10_TEX2D_DSV
author: windows-sdk-content
description: Specifies the subresource from a 2D texture that is accessible to a depth-stencil view.
old-location: direct3d10\d3d10_tex2d_dsv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2d_dsv.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_TEX2D_DSV, D3D10_TEX2D_DSV structure [Direct3D 10], c7842b23-969e-3b59-100f-750283b6b232, d3d10/D3D10_TEX2D_DSV, direct3d10.d3d10_tex2d_dsv
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D10_TEX2D_DSV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX2D_DSV
req.redist: 
---

# D3D10_TEX2D_DSV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a> from a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a> that is accessible to a depth-stencil view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first mipmap level to use (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">mip slice</a>).


## -remarks



This structure is one member of a depth-stencil-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205037(v=VS.85).aspx">D3D10_DEPTH_STENCIL_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

