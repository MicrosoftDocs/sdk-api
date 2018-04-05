---
UID: NN:d3d11.ID3D11DepthStencilView
title: ID3D11DepthStencilView
author: windows-driver-content
description: A depth-stencil-view interface accesses a texture resource during depth-stencil testing.
old-location: direct3d11\id3d11depthstencilview.htm
old-project: direct3d11
ms.assetid: 10be1fd1-8700-4c0a-b447-d3c2569f8e81
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 5e846266-8e0b-d52b-2f70-8936cbeb0bd1, ID3D11DepthStencilView, ID3D11DepthStencilView interface [Direct3D 11], ID3D11DepthStencilView interface [Direct3D 11], described, d3d11/ID3D11DepthStencilView, direct3d11.id3d11depthstencilview
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DepthStencilView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DepthStencilView interface


## -description


A depth-stencil-view interface accesses a texture resource during depth-stencil testing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DepthStencilView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11DepthStencilView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/00fd30de-ceae-4bcb-8602-36d43edd17b1">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil view.

</td>
</tr>
</table> 


## -remarks



To create a depth-stencil view, call <a href="https://msdn.microsoft.com/b3e899eb-3df6-421f-bdc8-98d7c7acbe62">ID3D11Device::CreateDepthStencilView</a>.

To bind a depth-stencil view to the pipeline, call <a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">ID3D11DeviceContext::OMSetRenderTargets</a>.




## -see-also




<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

