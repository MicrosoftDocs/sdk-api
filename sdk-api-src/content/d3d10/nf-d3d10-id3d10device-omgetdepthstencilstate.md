---
UID: NF:d3d10.ID3D10Device.OMGetDepthStencilState
title: ID3D10Device::OMGetDepthStencilState
author: windows-sdk-content
description: Gets the depth-stencil state of the output-merger stage.
old-location: direct3d10\id3d10device_omgetdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetdepthstencilstate.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 5fead180-40d5-ddfe-7065-11f773e4032e, ID3D10Device interface [Direct3D 10],OMGetDepthStencilState method, ID3D10Device.OMGetDepthStencilState, ID3D10Device::OMGetDepthStencilState, OMGetDepthStencilState, OMGetDepthStencilState method [Direct3D 10], OMGetDepthStencilState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMGetDepthStencilState, direct3d10.id3d10device_omgetdepthstencilstate
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
 - ID3D10Device.OMGetDepthStencilState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::OMGetDepthStencilState


## -description


Gets the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> state of the output-merger stage.


## -parameters




### -param ppDepthStencilState [out]

Type: <b><a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>**</b>

Address of a pointer to a depth-stencil state interface (see <a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>) to be filled with information from the device.


### -param pStencilRef [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to the stencil reference value used in the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> test.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

