---
UID: NF:d3d11.ID3D11Device.CreateSamplerState
title: ID3D11Device::CreateSamplerState
author: windows-sdk-content
description: Create a sampler-state object that encapsulates sampling information for a texture.
old-location: direct3d11\id3d11device_createsamplerstate.htm
tech.root: direct3d11
ms.assetid: 66cf7189-2882-43a4-8732-657402c983db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 845db980-5abf-c948-258d-62903feec271, CreateSamplerState, CreateSamplerState method [Direct3D 11], CreateSamplerState method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateSamplerState method, ID3D11Device.CreateSamplerState, ID3D11Device::CreateSamplerState, d3d11/ID3D11Device::CreateSamplerState, direct3d11.id3d11device_createsamplerstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateSamplerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CreateSamplerState


## -description


Create a sampler-state object that encapsulates sampling information for a texture.


## -parameters




### -param pSamplerDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a>*</b>

Pointer to a sampler state description (see <a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a>).


### -param ppSamplerState [out, optional]

Type: <b><a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>**</b>

Address of a pointer to the sampler state object created (see <a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



4096 unique sampler state objects can be created on a device at a time.

If an application attempts to create a sampler-state interface with the same state as an existing interface, the same interface will be returned and the total number of unique sampler state objects will stay the same.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

