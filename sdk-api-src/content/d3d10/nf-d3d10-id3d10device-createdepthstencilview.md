---
UID: NF:d3d10.ID3D10Device.CreateDepthStencilView
title: ID3D10Device::CreateDepthStencilView
author: windows-sdk-content
description: Create a depth-stencil view for accessing resource data.
old-location: direct3d10\id3d10device_createdepthstencilview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createdepthstencilview.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateDepthStencilView, CreateDepthStencilView method [Direct3D 10], CreateDepthStencilView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateDepthStencilView method, ID3D10Device.CreateDepthStencilView, ID3D10Device::CreateDepthStencilView, d3d10/ID3D10Device::CreateDepthStencilView, direct3d10.id3d10device_createdepthstencilview, f7b0585b-710f-b4d1-e65f-c30b57116c09
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateDepthStencilView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.CreateDepthStencilView
: 
---

# ID3D10Device::CreateDepthStencilView


## -description


Create a depth-stencil <a href="https://msdn.microsoft.com/en-us/library/Bb205128(v=VS.85).aspx">view</a> for accessing resource data.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">resource</a> that will serve as the depth-stencil surface. This resource must have been created with the <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_DEPTH_STENCIL</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb205037(v=VS.85).aspx">D3D10_DEPTH_STENCIL_VIEW_DESC</a>*</b>

Pointer to a depth-stencil-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205037(v=VS.85).aspx">D3D10_DEPTH_STENCIL_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).


### -param ppDepthStencilView [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A depth-stencil view can be bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173597(v=VS.85).aspx">ID3D10Device::OMSetRenderTargets</a>.

For more background information, see the <a href="https://msdn.microsoft.com/en-us/library/Bb205074(v=VS.85).aspx">programming guide page</a> about depth stencils.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

