---
UID: NS:d3d10.D3D10_TEX3D_RTV
title: D3D10_TEX3D_RTV
author: windows-sdk-content
description: Specifies the subresource(s) from a 3D texture to use in a render-target view.
old-location: direct3d10\d3d10_tex3d_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex3d_rtv.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D10_TEX3D_RTV, D3D10_TEX3D_RTV structure [Direct3D 10], a846ce63-d213-1889-2297-8bc813006637, d3d10/D3D10_TEX3D_RTV, direct3d10.d3d10_tex3d_rtv
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
 - D3D10_TEX3D_RTV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX3D_RTV
req.redist: 
---

# D3D10_TEX3D_RTV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">3D texture</a> to use in a render-target view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the mipmap level to use (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">mip slice</a>).


### -field FirstWSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

First depth level to use.


### -field WSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of depth levels to use in the render-target view, starting from <b>FirstWSlice</b>. A value of -1 indicates all of the slices along the w axis, starting from <b>FirstWSlice</b>.


## -remarks



This structure is one member of a render target view. See <a href="https://msdn.microsoft.com/en-us/library/Bb172410(v=VS.85).aspx">D3D10_RENDER_TARGET_VIEW_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

