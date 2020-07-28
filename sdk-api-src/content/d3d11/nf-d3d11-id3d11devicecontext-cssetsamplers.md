---
UID: NF:d3d11.ID3D11DeviceContext.CSSetSamplers
title: ID3D11DeviceContext::CSSetSamplers (d3d11.h)
description: Set an array of sampler states to the compute-shader stage.
helpviewer_keywords: ["CSSetSamplers","CSSetSamplers method [Direct3D 11]","CSSetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSSetSamplers method","ID3D11DeviceContext.CSSetSamplers","ID3D11DeviceContext::CSSetSamplers","aa74392c-a8c7-cf2c-b761-f00d5b5b4fb9","d3d11/ID3D11DeviceContext::CSSetSamplers","direct3d11.id3d11devicecontext_cssetsamplers"]
old-location: direct3d11\id3d11devicecontext_cssetsamplers.htm
tech.root: direct3d11
ms.assetid: 8b7f5c6d-0d9d-4b8b-a812-1e2b3b7386e9
ms.date: 12/05/2018
ms.keywords: CSSetSamplers, CSSetSamplers method [Direct3D 11], CSSetSamplers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSSetSamplers method, ID3D11DeviceContext.CSSetSamplers, ID3D11DeviceContext::CSSetSamplers, aa74392c-a8c7-cf2c-b761-f00d5b5b4fb9, d3d11/ID3D11DeviceContext::CSSetSamplers, direct3d11.id3d11devicecontext_cssetsamplers
f1_keywords:
- d3d11/ID3D11DeviceContext.CSSetSamplers
dev_langs:
- c++
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
- ID3D11DeviceContext.CSSetSamplers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext::CSSetSamplers


## -description


Set an array of sampler states to the compute-shader stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).


### -param NumSamplers [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).


### -param ppSamplers [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>). See Remarks.


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




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
 

 

