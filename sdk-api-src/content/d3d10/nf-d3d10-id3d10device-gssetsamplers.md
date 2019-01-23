---
UID: NF:d3d10.ID3D10Device.GSSetSamplers
title: ID3D10Device::GSSetSamplers
author: windows-sdk-content
description: Set an array of sampler states to the geometry shader pipeline stage.
old-location: direct3d10\id3d10device_gssetsamplers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gssetsamplers.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 1c08811a-830c-451d-31b2-e679c42bcf69, GSSetSamplers, GSSetSamplers method [Direct3D 10], GSSetSamplers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSSetSamplers method, ID3D10Device.GSSetSamplers, ID3D10Device::GSSetSamplers, d3d10/ID3D10Device::GSSetSamplers, direct3d10.id3d10device_gssetsamplers
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
 - ID3D10Device.GSSetSamplers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::GSSetSamplers


## -description


Set an array of sampler states to the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">geometry shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to.


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available.


### -param ppSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="https://msdn.microsoft.com/en-us/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>). See Remarks.


## -returns



Returns nothing.




## -remarks



Any sampler may be set to <b>NULL</b>; this invokes the default state, which is defined to be the following.


```

//Default sampler state:
D3D10_SAMPLER_DESC SamplerDesc;
SamplerDesc.Filter = D3D10_FILTER_MIN_MAG_MIP_LINEAR;
SamplerDesc.AddressU = D3D10_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.AddressV = D3D10_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.AddressW = D3D10_TEXTURE_ADDRESS_CLAMP;
SamplerDesc.MipLODBias = 0;
SamplerDesc.MaxAnisotropy = 1;
SamplerDesc.ComparisonFunc = D3D10_COMPARISON_NEVER;
SamplerDesc.BorderColor[0] = 1.0f;
SamplerDesc.BorderColor[1] = 1.0f;
SamplerDesc.BorderColor[2] = 1.0f;
SamplerDesc.BorderColor[3] = 1.0f;
SamplerDesc.MinLOD = -FLT_MAX;
SamplerDesc.MaxLOD = FLT_MAX;
		
```


The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

