---
UID: NN:d3d11.ID3D11RenderTargetView
title: ID3D11RenderTargetView
author: windows-sdk-content
description: A render-target-view interface identifies the render-target subresources that can be accessed during rendering.
old-location: direct3d11\id3d11rendertargetview.htm
tech.root: direct3d11
ms.assetid: 3ae7c255-2403-493a-9fb9-fc9795f6d920
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11RenderTargetView, ID3D11RenderTargetView interface [Direct3D 11], ID3D11RenderTargetView interface [Direct3D 11],described, d3d11/ID3D11RenderTargetView, direct3d11.id3d11rendertargetview, ffd3acf9-f2dc-0823-23c9-1188e5ede6f2
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
 - ID3D11RenderTargetView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11RenderTargetView interface


## -description


A render-target-view interface identifies the render-target subresources that can be accessed during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RenderTargetView</b> interface inherits from <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>. <b>ID3D11RenderTargetView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11RenderTargetView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72aeb6c2-10a1-4deb-a3a5-1824e59b4bc8">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a render target view.

</td>
</tr>
</table> 


## -remarks



To create a render-target view, call <a href="https://msdn.microsoft.com/e757c959-f0ac-44c3-8226-b9f0b1c2a031">ID3D11Device::CreateRenderTargetView</a>. To bind a render-target view to the pipeline, call <a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">ID3D11DeviceContext::OMSetRenderTargets</a>.

A rendertarget is a resource that can be written by the output-merger stage at the end of a render pass. Each render-target should also have a corresponding depth-stencil view.




## -see-also




<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

