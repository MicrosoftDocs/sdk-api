---
UID: NN:d3d11.ID3D11DepthStencilView
title: ID3D11DepthStencilView
author: windows-sdk-content
description: A depth-stencil-view interface accesses a texture resource during depth-stencil testing.
old-location: direct3d11\id3d11depthstencilview.htm
tech.root: direct3d11
ms.assetid: 10be1fd1-8700-4c0a-b447-d3c2569f8e81
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 5e846266-8e0b-d52b-2f70-8936cbeb0bd1, ID3D11DepthStencilView, ID3D11DepthStencilView interface [Direct3D 11], ID3D11DepthStencilView interface [Direct3D 11],described, d3d11/ID3D11DepthStencilView, direct3d11.id3d11depthstencilview
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
 - ID3D11DepthStencilView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DepthStencilView interface


## -description


A depth-stencil-view interface accesses a texture resource during depth-stencil testing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DepthStencilView</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>. <b>ID3D11DepthStencilView</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11DepthStencilView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476378(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil view.

</td>
</tr>
</table> 


## -remarks



To create a depth-stencil view, call <a href="https://msdn.microsoft.com/en-us/library/Ff476507(v=VS.85).aspx">ID3D11Device::CreateDepthStencilView</a>.

To bind a depth-stencil view to the pipeline, call <a href="https://msdn.microsoft.com/en-us/library/Ff476464(v=VS.85).aspx">ID3D11DeviceContext::OMSetRenderTargets</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476642(v=VS.85).aspx">ID3D11View</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476172(v=VS.85).aspx">Resource Interfaces</a>
 

 

