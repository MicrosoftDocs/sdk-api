---
UID: NN:d3d10.ID3D10SamplerState
title: ID3D10SamplerState (d3d10.h)
author: windows-sdk-content
description: A sampler-state interface accesses sampler state for a texture.
old-location: direct3d10\id3d10samplerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10samplerstate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2116312d-356e-9f01-4cdf-78e47d9a4ae8, ID3D10SamplerState, ID3D10SamplerState interface [Direct3D 10], ID3D10SamplerState interface [Direct3D 10],described, d3d10/ID3D10SamplerState, direct3d10.id3d10samplerstate
ms.topic: interface
f1_keywords: 
 - "d3d10/ID3D10SamplerState"
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
 - ID3D10SamplerState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10SamplerState interface


## -description


A sampler-state interface accesses sampler state for a <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type">texture</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10SamplerState</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10SamplerState</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10samplerstate-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the sampler state.

</td>
</tr>
</table> 


## -remarks



Create a sampler-state object by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createsamplerstate">ID3D10Device::CreateSamplerState</a>.

To initialize sampler state, bind the sampler-state object to the pipeline by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetsamplers">ID3D10Device::VSSetSamplers</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetsamplers">ID3D10Device::GSSetSamplers</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetsamplers">ID3D10Device::PSSetSamplers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core">Core Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
 

 

