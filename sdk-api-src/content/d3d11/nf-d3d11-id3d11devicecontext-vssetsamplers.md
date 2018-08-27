---
UID: NF:d3d11.ID3D11DeviceContext.VSSetSamplers
title: ID3D11DeviceContext::VSSetSamplers
author: windows-sdk-content
description: Set an array of sampler states to the vertex shader pipeline stage.
old-location: direct3d11\id3d11devicecontext_vssetsamplers.htm
old-project: direct3d11
ms.assetid: bfbf557c-f355-4d4d-beb0-f36e1c6f32ed
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],VSSetSamplers method, ID3D11DeviceContext.VSSetSamplers, ID3D11DeviceContext::VSSetSamplers, VSSetSamplers, VSSetSamplers method [Direct3D 11], VSSetSamplers method [Direct3D 11],ID3D11DeviceContext interface, d33a9d82-8e5e-f982-a29f-bcaff20393ff, d3d11/ID3D11DeviceContext::VSSetSamplers, direct3d11.id3d11devicecontext_vssetsamplers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.VSSetSamplers
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::VSSetSamplers


## -description


Set an array of sampler states to the vertex shader pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).


### -param ppSamplers [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476588(v=VS.85).aspx">ID3D11SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="https://msdn.microsoft.com/en-us/library/Ff476588(v=VS.85).aspx">ID3D11SamplerState</a>). See Remarks.


## -returns



This method does not return a value.




## -remarks



Any sampler may be set to <b>NULL</b>; this invokes the default state, which is defined to be the following.


```

//Default sampler state:
D3D11_SAMPLER_DESC SamplerDesc;
SamplerDesc.Filter = D3D11_FILTER_MIN_MAG_MIP_LINEAR;
SamplerDesc.AddressU = D3D11_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.AddressV = D3D11_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.AddressW = D3D11_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.MipLODBias = 0;
SamplerDesc.MaxAnisotropy = 1;
SamplerDesc.ComparisonFunc = D3D11_COMPARISON_NEVER;
SamplerDesc.BorderColor[0] = 1.0f;
SamplerDesc.BorderColor[1] = 1.0f;
SamplerDesc.BorderColor[2] = 1.0f;
SamplerDesc.BorderColor[3] = 1.0f;
SamplerDesc.MinLOD = -FLT_MAX;
SamplerDesc.MaxLOD = FLT_MAX;
		
```


The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

