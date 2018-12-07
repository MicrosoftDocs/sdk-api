---
UID: NF:d3d10.ID3D10Device.OMGetRenderTargets
title: ID3D10Device::OMGetRenderTargets
author: windows-sdk-content
description: Get pointers to the render targets and the depth-stencil buffer that are available to the output-merger stage.
old-location: direct3d10\id3d10device_omgetrendertargets.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetrendertargets.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10Device interface [Direct3D 10],OMGetRenderTargets method, ID3D10Device.OMGetRenderTargets, ID3D10Device::OMGetRenderTargets, OMGetRenderTargets, OMGetRenderTargets method [Direct3D 10], OMGetRenderTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMGetRenderTargets, direct3d10.id3d10device_omgetrendertargets, f378deb9-1829-aecc-36fe-7c3ab163d523
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
 - ID3D10Device.OMGetRenderTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::OMGetRenderTargets


## -description


Get pointers to the render targets and the depth-stencil buffer that are available to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a>.


## -parameters




### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of render targets to retrieve.


### -param ppRenderTargetViews [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView</a>**</b>

Pointer to an array of render targets views (see <a href="https://msdn.microsoft.com/en-us/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView</a>) to be filled with the render targets from the device. Specify <b>NULL</b> for this parameter when retrieval of a render target is not needed. 


### -param ppDepthStencilView [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>**</b>

Pointer to a depth-stencil view (see <a href="https://msdn.microsoft.com/en-us/library/Bb173526(v=VS.85).aspx">ID3D10DepthStencilView</a>) to be filled with the depth-stencil information from the device. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not needed.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

