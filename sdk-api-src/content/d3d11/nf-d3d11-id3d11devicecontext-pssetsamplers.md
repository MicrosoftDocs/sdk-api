---
UID: NF:d3d11.ID3D11DeviceContext.PSSetSamplers
title: ID3D11DeviceContext::PSSetSamplers
author: windows-sdk-content
description: Set an array of sampler states to the pixel shader pipeline stage.
old-location: direct3d11\id3d11devicecontext_pssetsamplers.htm
tech.root: direct3d11
ms.assetid: b344c0fb-056d-452d-9d30-a8f97e7d226a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],PSSetSamplers method, ID3D11DeviceContext.PSSetSamplers, ID3D11DeviceContext::PSSetSamplers, PSSetSamplers, PSSetSamplers method [Direct3D 11], PSSetSamplers method [Direct3D 11],ID3D11DeviceContext interface, bedb6ab1-e7ea-70b9-097a-00978aae4f00, d3d11/ID3D11DeviceContext::PSSetSamplers, direct3d11.id3d11devicecontext_pssetsamplers
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
 - ID3D11DeviceContext.PSSetSamplers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::PSSetSamplers


## -description


Set an array of sampler states to the pixel shader pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).


### -param ppSamplers [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>). See Remarks.


## -returns



This method does not return a value.




## -remarks



Any sampler may be set to <b>NULL</b>; this invokes the default state, which is defined to be the following.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>Filter</td>
<td>D3D11_FILTER_MIN_MAG_MIP_LINEAR</td>
</tr>
<tr>
<td>AddressU</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressV</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressW</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>MipLODBias</td>
<td>0</td>
</tr>
<tr>
<td>MaxAnisotropy</td>
<td>1</td>
</tr>
<tr>
<td>ComparisonFunc</td>
<td>D3D11_COMPARISON_NEVER</td>
</tr>
<tr>
<td>BorderColor[0]</td>
<td>1.0f</td>
</tr>
<tr>
<td>BorderColor[1]</td>
<td>1.0f</td>
</tr>
<tr>
<td>BorderColor[2]</td>
<td>1.0f</td>
</tr>
<tr>
<td>BorderColor[3]</td>
<td>1.0f</td>
</tr>
<tr>
<td>MinLOD</td>
<td>-FLT_MAX</td>
</tr>
<tr>
<td>MaxLOD</td>
<td>FLT_MAX</td>
</tr>
</table>
 

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

