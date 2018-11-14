---
UID: NF:d3d10.ID3D10Device.CreateDepthStencilState
title: ID3D10Device::CreateDepthStencilState
author: windows-sdk-content
description: Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage.
old-location: direct3d10\id3d10device_createdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createdepthstencilstate.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateDepthStencilState, CreateDepthStencilState method [Direct3D 10], CreateDepthStencilState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateDepthStencilState method, ID3D10Device.CreateDepthStencilState, ID3D10Device::CreateDepthStencilState, a3a47d35-efaa-1c5f-3cb4-492e0e20a0b0, d3d10/ID3D10Device::CreateDepthStencilState, direct3d10.id3d10device_createdepthstencilstate
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
 - ID3D10Device.CreateDepthStencilState
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
- ID3D10Device.CreateDepthStencilState
: 
---

# ID3D10Device::CreateDepthStencilState


## -description


Create a depth-stencil state object that encapsulates <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil test</a> information for the output-merger stage.


## -parameters




### -param pDepthStencilDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a>*</b>

Pointer to a depth-stencil state description (see <a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a>).


### -param ppDepthStencilState [out]

Type: <b><a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState</a>**</b>

Address of a pointer to the depth-stencil state object created (see <a href="https://msdn.microsoft.com/7cb79259-5575-4307-ab02-8bf11a0acf90">ID3D10DepthStencilState Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



4096 unique depth-stencil state objects can be created on a device at a time.

If an application attempts to create a depth-stencil state with the same description as an already existing depth-stencil state, then the same interface with an incremented reference count will be returned and the total number of unique depth-stencil state objects will stay the same.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

