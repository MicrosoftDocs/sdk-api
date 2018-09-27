---
UID: NN:d3d11.ID3D11RasterizerState
title: ID3D11RasterizerState
author: windows-sdk-content
description: The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage.
old-location: direct3d11\id3d11rasterizerstate.htm
tech.root: direct3d11
ms.assetid: fbe6d2b9-375e-4390-9d34-36acef0a5aa2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 6b2716ca-7676-6b26-071d-20ec80705737, ID3D11RasterizerState, ID3D11RasterizerState interface [Direct3D 11], ID3D11RasterizerState interface [Direct3D 11],described, d3d11/ID3D11RasterizerState, direct3d11.id3d11rasterizerstate
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
 - ID3D11RasterizerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11RasterizerState interface


## -description


The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RasterizerState</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11RasterizerState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11RasterizerState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc6bbdd2-af9c-45be-a13a-5f9105f08c99">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description for rasterizer state that you used to create the rasterizer-state object.

</td>
</tr>
</table> 


## -remarks



To create a rasterizer-state object, call <a href="https://msdn.microsoft.com/b49a8dbb-2280-4d5d-ae65-58cde2e9ed10">ID3D11Device::CreateRasterizerState</a>. To bind the rasterizer-state object to the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>, call <a href="https://msdn.microsoft.com/aa76cd3f-5d08-48e7-bd38-ff4d7119eae3">ID3D11DeviceContext::RSSetState</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>
 

 

