---
UID: NN:d3d11_3.ID3D11RenderTargetView1
title: ID3D11RenderTargetView1
author: windows-sdk-content
description: A render-target-view interface represents the render-target subresources that can be accessed during rendering.
old-location: direct3d11\id3d11rendertargetview1.htm
tech.root: direct3d11
ms.assetid: 6063229D-A85A-46E8-9034-D1C2C26A5274
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11RenderTargetView1, ID3D11RenderTargetView1 interface [Direct3D 11], ID3D11RenderTargetView1 interface [Direct3D 11],described, d3d11_3/ID3D11RenderTargetView1, direct3d11.id3d11rendertargetview1
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
 - ID3D11RenderTargetView1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11RenderTargetView1 interface


## -description


A render-target-view interface represents the render-target subresources that can be accessed during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11RenderTargetView1</b> interface inherits from <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>. <b>ID3D11RenderTargetView1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11RenderTargetView1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5AC36368-64DC-46C3-ACF4-36E5133019D8">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets the properties of a render-target view.

</td>
</tr>
</table> 


## -remarks



To create a render-target view, call <a href="https://msdn.microsoft.com/9B85B007-F8B0-43C1-999E-75E5243B7B5A">ID3D11Device3::CreateRenderTargetView1</a>. To bind a render-target view to the pipeline, call <a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">ID3D11DeviceContext::OMSetRenderTargets</a>.

A render target is a resource that can be written by the output-merger stage at the end of a render pass. Each render target can also have a corresponding depth-stencil view.




## -see-also




<a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>



<a href="https://msdn.microsoft.com/8e40573a-b186-41ec-b2ff-81279d77bd3a">Resource Interfaces</a>
 

 

