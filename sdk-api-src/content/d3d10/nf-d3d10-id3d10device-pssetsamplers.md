---
UID: NF:d3d10.ID3D10Device.PSSetSamplers
title: ID3D10Device::PSSetSamplers (d3d10.h)
description: Set an array of sampler states to the pixel shader pipeline stage. (ID3D10Device.PSSetSamplers)
helpviewer_keywords: ["5f7069fa-43fc-1459-30dc-3cb118f8bb46","ID3D10Device interface [Direct3D 10]","PSSetSamplers method","ID3D10Device.PSSetSamplers","ID3D10Device::PSSetSamplers","PSSetSamplers","PSSetSamplers method [Direct3D 10]","PSSetSamplers method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::PSSetSamplers","direct3d10.id3d10device_pssetsamplers"]
old-location: direct3d10\id3d10device_pssetsamplers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetsamplers.htm
ms.date: 12/05/2018
ms.keywords: 5f7069fa-43fc-1459-30dc-3cb118f8bb46, ID3D10Device interface [Direct3D 10],PSSetSamplers method, ID3D10Device.PSSetSamplers, ID3D10Device::PSSetSamplers, PSSetSamplers, PSSetSamplers method [Direct3D 10], PSSetSamplers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSSetSamplers, direct3d10.id3d10device_pssetsamplers
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::PSSetSamplers
 - d3d10/ID3D10Device::PSSetSamplers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.PSSetSamplers
---

# ID3D10Device::PSSetSamplers


## -description

Set an array of sampler states to the <a href="/previous-versions/bb205146(v=vs.85)">pixel shader</a> pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to.

### -param NumSamplers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available.

### -param ppSamplers [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>). See Remarks.

## -remarks

Any sampler may be set to <b>NULL</b>; this invokes the default state, which is defined to be the following.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>Filter</td>
<td>D3D10_FILTER_MIN_MAG_MIP_LINEAR</td>
</tr>
<tr>
<td>AddressU</td>
<td>D3D10_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressV</td>
<td>D3D10_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressW</td>
<td>D3D10_TEXTURE_ADDRESS_CLAMP</td>
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
<td>D3D10_COMPARISON_NEVER</td>
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
 

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
