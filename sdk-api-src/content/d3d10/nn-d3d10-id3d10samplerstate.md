---
UID: NN:d3d10.ID3D10SamplerState
title: ID3D10SamplerState
author: windows-sdk-content
description: A sampler-state interface accesses sampler state for a texture.
old-location: direct3d10\id3d10samplerstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10samplerstate.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 2116312d-356e-9f01-4cdf-78e47d9a4ae8, ID3D10SamplerState, ID3D10SamplerState interface [Direct3D 10], ID3D10SamplerState interface [Direct3D 10],described, d3d10/ID3D10SamplerState, direct3d10.id3d10samplerstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID3D10SamplerState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10SamplerState interface


## -description


A sampler-state interface accesses sampler state for a <a href="https://msdn.microsoft.com/e8cb483a-d831-4942-b6fe-61dd5edb1813">texture</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10SamplerState</b> interface inherits from <a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>. <b>ID3D10SamplerState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10SamplerState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a89bb8c8-b12a-4982-9cea-d03ca76b2a0e">GetDesc</a>
</td>
<td align="left" width="63%">
Get the sampler state.

</td>
</tr>
</table> 


## -remarks



Create a sampler-state object by calling <a href="https://msdn.microsoft.com/82dea278-1555-49b8-9c1d-91399afa5c7e">ID3D10Device::CreateSamplerState</a>.

To initialize sampler state, bind the sampler-state object to the pipeline by calling <a href="https://msdn.microsoft.com/4310c4dc-7fb4-4b69-9bc5-e89761d2e34c">ID3D10Device::VSSetSamplers</a>, <a href="https://msdn.microsoft.com/881cea8b-eb37-4614-b4dc-81a3e8c929d3">ID3D10Device::GSSetSamplers</a>, or <a href="https://msdn.microsoft.com/2684b37d-8f10-4c32-8c52-fc2e5bf2122c">ID3D10Device::PSSetSamplers</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/0b217811-555e-4433-8cf8-8c43cd5edba6">Core Reference</a>



<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>
 

 

