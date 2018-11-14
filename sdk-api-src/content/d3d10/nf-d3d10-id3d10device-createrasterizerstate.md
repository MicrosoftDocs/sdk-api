---
UID: NF:d3d10.ID3D10Device.CreateRasterizerState
title: ID3D10Device::CreateRasterizerState
author: windows-sdk-content
description: Create a rasterizer state object that tells the rasterizer stage how to behave.
old-location: direct3d10\id3d10device_createrasterizerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createrasterizerstate.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateRasterizerState, CreateRasterizerState method [Direct3D 10], CreateRasterizerState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateRasterizerState method, ID3D10Device.CreateRasterizerState, ID3D10Device::CreateRasterizerState, b5877d5f-3976-076e-eb6a-ddf73c6f4995, d3d10/ID3D10Device::CreateRasterizerState, direct3d10.id3d10device_createrasterizerstate
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
 - ID3D10Device.CreateRasterizerState
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
- ID3D10Device.CreateRasterizerState
: 
---

# ID3D10Device::CreateRasterizerState


## -description


Create a rasterizer state object that tells the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> how to behave.


## -parameters




### -param pRasterizerDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">D3D10_RASTERIZER_DESC</a>*</b>

Pointer to a rasterizer state description (see <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">D3D10_RASTERIZER_DESC</a>).


### -param ppRasterizerState [out]

Type: <b><a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState</a>**</b>

Address of a pointer to the rasterizer state object created (see <a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



4096 unique rasterizer state objects can be created on a device at a time.

If an application attempts to create a rasterizer state with the same description as an already existing rasterizer state, then the same interface with an incremented reference count will be returned and the total number of unique rasterizer state objects will stay the same.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

