---
UID: NF:d3d10.ID3D10Device.CreateSamplerState
title: ID3D10Device::CreateSamplerState
author: windows-sdk-content
description: Create a sampler-state object that encapsulates sampling information for a texture.
old-location: direct3d10\id3d10device_createsamplerstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createsamplerstate.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateSamplerState, CreateSamplerState method [Direct3D 10], CreateSamplerState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateSamplerState method, ID3D10Device.CreateSamplerState, ID3D10Device::CreateSamplerState, a31393bc-fcc0-a2f3-9886-f79cb4ca7009, d3d10/ID3D10Device::CreateSamplerState, direct3d10.id3d10device_createsamplerstate
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
 - ID3D10Device.CreateSamplerState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateSamplerState


## -description


Create a sampler-state object that encapsulates sampling information for a <a href="https://msdn.microsoft.com/e8cb483a-d831-4942-b6fe-61dd5edb1813">texture</a>.


## -parameters




### -param pSamplerDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/b97db311-de57-45f3-a6dd-8af768b2680d">D3D10_SAMPLER_DESC</a>*</b>

Pointer to a sampler state description (see <a href="https://msdn.microsoft.com/b97db311-de57-45f3-a6dd-8af768b2680d">D3D10_SAMPLER_DESC</a>).


### -param ppSamplerState [out]

Type: <b><a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState</a>**</b>

Address of a pointer to the sampler state object created (see <a href="https://msdn.microsoft.com/5815f809-aec0-49b1-bcef-d04146551af9">ID3D10SamplerState Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



4096 unique sampler state objects can be created on a device at a time.

If an application attempts to create a sampler state with the same description as an already existing sampler state, then the same interface with an incremented reference count will be returned and the total number of unique sampler state objects will stay the same.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

