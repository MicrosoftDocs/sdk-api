---
UID: NF:d3d10.ID3D10Device.CreateRenderTargetView
title: ID3D10Device::CreateRenderTargetView
author: windows-sdk-content
description: Create a render-target view for accessing resource data.
old-location: direct3d10\id3d10device_createrendertargetview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createrendertargetview.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 080acf2e-83e1-3be3-60d6-8385a6585f49, CreateRenderTargetView, CreateRenderTargetView method [Direct3D 10], CreateRenderTargetView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateRenderTargetView method, ID3D10Device.CreateRenderTargetView, ID3D10Device::CreateRenderTargetView, d3d10/ID3D10Device::CreateRenderTargetView, direct3d10.id3d10device_createrendertargetview
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateRenderTargetView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateRenderTargetView


## -description


Create a render-target <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a> for accessing resource data.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173829(v=VS.85).aspx">ID3D10Resource</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/library/Bb205133(v=VS.85).aspx">resource</a> that will serve as the render target. This resource must have been created with the <a href="https://msdn.microsoft.com/library/Bb204891(v=VS.85).aspx">D3D10_BIND_RENDER_TARGET</a> flag.


### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb172410(v=VS.85).aspx">D3D10_RENDER_TARGET_VIEW_DESC</a>*</b>

Pointer to a render-target-view description (see <a href="https://msdn.microsoft.com/library/Bb172410(v=VS.85).aspx">D3D10_RENDER_TARGET_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).


### -param ppRTView [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A rendertarget view can be bound to the <a href="https://msdn.microsoft.com/library/Bb205120(v=VS.85).aspx">output merger stage</a> by calling <a href="https://msdn.microsoft.com/library/Bb173597(v=VS.85).aspx">ID3D10Device::OMSetRenderTargets</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

