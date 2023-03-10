---
UID: NF:d3d11.ID3D11DeviceContext.GSSetSamplers
title: ID3D11DeviceContext::GSSetSamplers (d3d11.h)
description: Set an array of sampler states to the geometry shader pipeline stage. (ID3D11DeviceContext.GSSetSamplers)
helpviewer_keywords: ["87e3b7dd-7f6c-9d28-cac9-47363e4c5207","GSSetSamplers","GSSetSamplers method [Direct3D 11]","GSSetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GSSetSamplers method","ID3D11DeviceContext.GSSetSamplers","ID3D11DeviceContext::GSSetSamplers","d3d11/ID3D11DeviceContext::GSSetSamplers","direct3d11.id3d11devicecontext_gssetsamplers"]
old-location: direct3d11\id3d11devicecontext_gssetsamplers.htm
tech.root: direct3d11
ms.assetid: 8e624e36-692e-4710-a267-05b73a089cd9
ms.date: 12/05/2018
ms.keywords: 87e3b7dd-7f6c-9d28-cac9-47363e4c5207, GSSetSamplers, GSSetSamplers method [Direct3D 11], GSSetSamplers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSSetSamplers method, ID3D11DeviceContext.GSSetSamplers, ID3D11DeviceContext::GSSetSamplers, d3d11/ID3D11DeviceContext::GSSetSamplers, direct3d11.id3d11devicecontext_gssetsamplers
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::GSSetSamplers
 - d3d11/ID3D11DeviceContext::GSSetSamplers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GSSetSamplers
---

# ID3D11DeviceContext::GSSetSamplers


## -description

Set an array of sampler states to the geometry shader pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).

### -param NumSamplers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).

### -param ppSamplers [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>). See Remarks.

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

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
