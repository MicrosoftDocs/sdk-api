---
UID: NN:d3d10.ID3D10SamplerState
title: ID3D10SamplerState
author: windows-sdk-content
description: A sampler-state interface accesses sampler state for a texture.
old-location: direct3d10\id3d10samplerstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10samplerstate.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
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


A sampler-state interface accesses sampler state for a <a href="https://msdn.microsoft.com/library/Bb509700(v=VS.85).aspx">texture</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10SamplerState</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10SamplerState</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/Bb173834(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the sampler state.

</td>
</tr>
</table> 


## -remarks



Create a sampler-state object by calling <a href="https://msdn.microsoft.com/library/Bb173557(v=VS.85).aspx">ID3D10Device::CreateSamplerState</a>.

To initialize sampler state, bind the sampler-state object to the pipeline by calling <a href="https://msdn.microsoft.com/library/Bb173627(v=VS.85).aspx">ID3D10Device::VSSetSamplers</a>, <a href="https://msdn.microsoft.com/library/Bb173581(v=VS.85).aspx">ID3D10Device::GSSetSamplers</a>, or <a href="https://msdn.microsoft.com/library/Bb173604(v=VS.85).aspx">ID3D10Device::PSSetSamplers</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb205149(v=VS.85).aspx">Core Reference</a>



<a href="https://msdn.microsoft.com/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>
 

 

