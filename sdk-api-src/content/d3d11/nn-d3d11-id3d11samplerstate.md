---
UID: NN:d3d11.ID3D11SamplerState
title: ID3D11SamplerState (d3d11.h)
author: windows-sdk-content
description: The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the pipeline for reference by texture sample operations.
old-location: direct3d11\id3d11samplerstate.htm
tech.root: direct3d11
ms.assetid: 8dc2facc-4f51-4064-aab4-028a06b9d7e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 10df1118-2f5f-fe2c-97bb-9adf4d72bc25, ID3D11SamplerState, ID3D11SamplerState interface [Direct3D 11], ID3D11SamplerState interface [Direct3D 11],described, d3d11/ID3D11SamplerState, direct3d11.id3d11samplerstate
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11SamplerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11SamplerState interface


## -description


The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="https://msdn.microsoft.com/8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc">pipeline</a> for reference by texture sample operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11SamplerState</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11SamplerState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11SamplerState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cca7f0f1-44b7-4f49-9149-acb12d745890">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description for sampler state that you used to create the sampler-state object.

</td>
</tr>
</table> 


## -remarks



To create a sampler-state object, call <a href="https://msdn.microsoft.com/66cf7189-2882-43a4-8732-657402c983db">ID3D11Device::CreateSamplerState</a>.

To bind a sampler-state object to any <a href="https://msdn.microsoft.com/8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc">pipeline</a> shader stage, call the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/bfbf557c-f355-4d4d-beb0-f36e1c6f32ed">ID3D11DeviceContext::VSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f573f65b-abd4-4ddd-9471-032c2c5552d7">ID3D11DeviceContext::HSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/15cc8f81-2d57-4148-821c-0136c0ce3f82">ID3D11DeviceContext::DSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8e624e36-692e-4710-a267-05b73a089cd9">ID3D11DeviceContext::GSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b344c0fb-056d-452d-9d30-a8f97e7d226a">ID3D11DeviceContext::PSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8b7f5c6d-0d9d-4b8b-a812-1e2b3b7386e9">ID3D11DeviceContext::CSSetSamplers</a>
</li>
</ul>
You can bind the same sampler-state object to multiple shader stages simultaneously.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

