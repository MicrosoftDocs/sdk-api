---
UID: NN:d3d11.ID3D11RasterizerState
title: ID3D11RasterizerState (d3d11.h)
author: windows-sdk-content
description: The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage.
old-location: direct3d11\id3d11rasterizerstate.htm
tech.root: direct3d11
ms.assetid: fbe6d2b9-375e-4390-9d34-36acef0a5aa2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6b2716ca-7676-6b26-071d-20ec80705737, ID3D11RasterizerState, ID3D11RasterizerState interface [Direct3D 11], ID3D11RasterizerState interface [Direct3D 11],described, d3d11/ID3D11RasterizerState, direct3d11.id3d11rasterizerstate
ms.topic: interface
f1_keywords: 
 - "d3d11/ID3D11RasterizerState"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11RasterizerState interface


## -description


The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RasterizerState</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11RasterizerState</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11rasterizerstate-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the description for rasterizer state that you used to create the rasterizer-state object.

</td>
</tr>
</table> 


## -remarks



To create a rasterizer-state object, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrasterizerstate">ID3D11Device::CreateRasterizerState</a>. To bind the rasterizer-state object to the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">ID3D11DeviceContext::RSSetState</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
 

 

