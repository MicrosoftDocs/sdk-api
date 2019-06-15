---
UID: NN:d3d11_3.ID3D11RasterizerState2
title: ID3D11RasterizerState2 (d3d11_3.h)
author: windows-sdk-content
description: The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage. This rasterizer-state interface supports forced sample count and conservative rasterization mode.
old-location: direct3d11\id3d11rasterizerstate2.htm
tech.root: direct3d11
ms.assetid: 335D976C-9E7F-4EAE-B671-F99D1B31669B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11RasterizerState2, ID3D11RasterizerState2 interface [Direct3D 11], ID3D11RasterizerState2 interface [Direct3D 11],described, d3d11_3/ID3D11RasterizerState2, direct3d11.id3d11rasterizerstate2
ms.topic: interface
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11RasterizerState2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11RasterizerState2 interface


## -description


The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>. This rasterizer-state interface supports forced sample count and conservative rasterization mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RasterizerState2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11rasterizerstate1">ID3D11RasterizerState1</a>. <b>ID3D11RasterizerState2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11RasterizerState2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11rasterizerstate2-getdesc2">GetDesc2</a>
</td>
<td align="left" width="63%">
Gets the description for rasterizer state that you used to create the rasterizer-state object.

</td>
</tr>
</table> 


## -remarks



To create a rasterizer-state object, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createrasterizerstate2">ID3D11Device3::CreateRasterizerState2</a>. To bind the rasterizer-state object to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">ID3D11DeviceContext::RSSetState</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11rasterizerstate1">ID3D11RasterizerState1</a>
 

 

