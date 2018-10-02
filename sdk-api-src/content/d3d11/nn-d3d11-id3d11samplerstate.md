---
UID: NN:d3d11.ID3D11SamplerState
title: ID3D11SamplerState
author: windows-sdk-content
description: The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the pipeline for reference by texture sample operations.
old-location: direct3d11\id3d11samplerstate.htm
tech.root: direct3d11
ms.assetid: 8dc2facc-4f51-4064-aab4-028a06b9d7e6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 10df1118-2f5f-fe2c-97bb-9adf4d72bc25, ID3D11SamplerState, ID3D11SamplerState interface [Direct3D 11], ID3D11SamplerState interface [Direct3D 11],described, d3d11/ID3D11SamplerState, direct3d11.id3d11samplerstate
ms.prod: windows
ms.technology: windows-sdk
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


The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="https://msdn.microsoft.com/en-us/library/Ff476882(v=VS.85).aspx">pipeline</a> for reference by texture sample operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11SamplerState</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11SamplerState</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476589(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description for sampler state that you used to create the sampler-state object.

</td>
</tr>
</table> 


## -remarks



To create a sampler-state object, call <a href="https://msdn.microsoft.com/en-us/library/Ff476518(v=VS.85).aspx">ID3D11Device::CreateSamplerState</a>.

To bind a sampler-state object to any <a href="https://msdn.microsoft.com/en-us/library/Ff476882(v=VS.85).aspx">pipeline</a> shader stage, call the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476492(v=VS.85).aspx">ID3D11DeviceContext::VSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476446(v=VS.85).aspx">ID3D11DeviceContext::HSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476419(v=VS.85).aspx">ID3D11DeviceContext::DSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476437(v=VS.85).aspx">ID3D11DeviceContext::GSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476471(v=VS.85).aspx">ID3D11DeviceContext::PSSetSamplers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476401(v=VS.85).aspx">ID3D11DeviceContext::CSSetSamplers</a>
</li>
</ul>
You can bind the same sampler-state object to multiple shader stages simultaneously.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

