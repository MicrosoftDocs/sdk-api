---
UID: NF:d3d10.ID3D10Device.PSSetSamplers
title: ID3D10Device::PSSetSamplers
author: windows-sdk-content
description: Set an array of sampler states to the pixel shader pipeline stage.
old-location: direct3d10\id3d10device_pssetsamplers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetsamplers.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5f7069fa-43fc-1459-30dc-3cb118f8bb46, ID3D10Device interface [Direct3D 10],PSSetSamplers method, ID3D10Device.PSSetSamplers, ID3D10Device::PSSetSamplers, PSSetSamplers, PSSetSamplers method [Direct3D 10], PSSetSamplers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSSetSamplers, direct3d10.id3d10device_pssetsamplers
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
 - ID3D10Device.PSSetSamplers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::PSSetSamplers


## -description


Set an array of sampler states to the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin setting samplers to.


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of samplers in the array. Each pipeline stage has a total of 16 sampler slots available.


### -param ppSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>*</b>

Pointer to an array of sampler-state interfaces (see <a href="https://msdn.microsoft.com/library/Bb173833(v=VS.85).aspx">ID3D10SamplerState</a>). See Remarks.


## -returns



Returns nothing.




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




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

