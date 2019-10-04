---
UID: NF:d3d10.ID3D10Device.CreateSamplerState
title: ID3D10Device::CreateSamplerState (d3d10.h)
author: windows-sdk-content
description: Create a sampler-state object that encapsulates sampling information for a texture.
old-location: direct3d10\id3d10device_createsamplerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createsamplerstate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSamplerState, CreateSamplerState method [Direct3D 10], CreateSamplerState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateSamplerState method, ID3D10Device.CreateSamplerState, ID3D10Device::CreateSamplerState, a31393bc-fcc0-a2f3-9886-f79cb4ca7009, d3d10/ID3D10Device::CreateSamplerState, direct3d10.id3d10device_createsamplerstate
ms.topic: method
f1_keywords: 
 - "d3d10/ID3D10Device.CreateSamplerState"
dev_langs:
 - c++
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
 - ID3D10Device.CreateSamplerState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::CreateSamplerState


## -description


Create a sampler-state object that encapsulates sampling information for a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type">texture</a>.


## -parameters




### -param pSamplerDesc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a>*</b>

Pointer to a sampler state description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a>).


### -param ppSamplerState [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>**</b>

Address of a pointer to the sampler state object created (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState Interface</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



4096 unique sampler state objects can be created on a device at a time.

If an application attempts to create a sampler state with the same description as an already existing sampler state, then the same interface with an incremented reference count will be returned and the total number of unique sampler state objects will stay the same.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

