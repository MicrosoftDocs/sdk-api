---
UID: NF:d3d10.ID3D10Device.OMGetRenderTargets
title: ID3D10Device::OMGetRenderTargets
author: windows-sdk-content
description: Get pointers to the render targets and the depth-stencil buffer that are available to the output-merger stage.
old-location: direct3d10\id3d10device_omgetrendertargets.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetrendertargets.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10Device interface [Direct3D 10],OMGetRenderTargets method, ID3D10Device.OMGetRenderTargets, ID3D10Device::OMGetRenderTargets, OMGetRenderTargets, OMGetRenderTargets method [Direct3D 10], OMGetRenderTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMGetRenderTargets, direct3d10.id3d10device_omgetrendertargets, f378deb9-1829-aecc-36fe-7c3ab163d523
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
 - ID3D10Device.OMGetRenderTargets
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::OMGetRenderTargets


## -description


Get pointers to the render targets and the depth-stencil buffer that are available to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.


## -parameters




### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of render targets to retrieve.


### -param ppRenderTargetViews [out]

Type: <b><a href="https://msdn.microsoft.com/0a545476-19d2-41f7-9012-82fbf633f23b">ID3D10RenderTargetView</a>**</b>

Pointer to an array of render targets views (see <a href="https://msdn.microsoft.com/0a545476-19d2-41f7-9012-82fbf633f23b">ID3D10RenderTargetView</a>) to be filled with the render targets from the device. Specify <b>NULL</b> for this parameter when retrieval of a render target is not needed. 


### -param ppDepthStencilView [out]

Type: <b><a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>**</b>

Pointer to a depth-stencil view (see <a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>) to be filled with the depth-stencil information from the device. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not needed.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

