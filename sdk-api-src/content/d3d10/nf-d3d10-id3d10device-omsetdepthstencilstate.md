---
UID: NF:d3d10.ID3D10Device.OMSetDepthStencilState
title: ID3D10Device::OMSetDepthStencilState
author: windows-sdk-content
description: Sets the depth-stencil state of the output-merger stage.
old-location: direct3d10\id3d10device_omsetdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omsetdepthstencilstate.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 75af58f4-0720-3b37-1633-f4ae71d23ebd, ID3D10Device interface [Direct3D 10],OMSetDepthStencilState method, ID3D10Device.OMSetDepthStencilState, ID3D10Device::OMSetDepthStencilState, OMSetDepthStencilState, OMSetDepthStencilState method [Direct3D 10], OMSetDepthStencilState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMSetDepthStencilState, direct3d10.id3d10device_omsetdepthstencilstate
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
 - ID3D10Device.OMSetDepthStencilState
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
- ID3D10Device.OMSetDepthStencilState
: 
---

# ID3D10Device::OMSetDepthStencilState


## -description


Sets the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> state of 
    the output-merger stage.


## -parameters




### -param pDepthStencilState [in]

Type: <b><a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>*</b>

Pointer to a depth-stencil state interface (see <a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>) to bind to the device.


### -param StencilRef [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reference value to perform against when doing a depth-stencil test. See remarks.


## -returns



Returns nothing.




## -remarks



To create a depth-stencil state interface, call <a href="https://msdn.microsoft.com/41dab20f-53e7-488d-a0c5-7435122d81b8">ID3D10Device::CreateDepthStencilState</a>.

Depth-stencil state is used by the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger</a> stage to 
      setup depth-stencil testing. 
      The stencil reference value is the control value used in the depth-stencil test.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an 
      interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

