---
UID: NN:d3d10.ID3D10View
title: ID3D10View
author: windows-sdk-content
description: A view interface specifies the parts of a resource the pipeline can access during rendering (see view).
old-location: direct3d10\id3d10view.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10view.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10View, ID3D10View interface [Direct3D 10], ID3D10View interface [Direct3D 10],described, d3d10/ID3D10View, direct3d10.id3d10view, f36206a8-55f1-ac58-4818-8c308ce6e81f
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10View
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10View interface


## -description


A view interface specifies the parts of a resource the pipeline can access during rendering (see <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a>).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10View</b> interface inherits from <a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>. <b>ID3D10View</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10View</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fcff4d7-3e9b-4fd6-a35a-a9c66ea10543">GetResource</a>
</td>
<td align="left" width="63%">
Get the resource that is accessed through this view.

</td>
</tr>
</table> 


## -remarks



A view interface is the base interface for all views. There are three types of views; a depth-stencil view, a render-target view, and a shader-resource view.

<ul>
<li>To create a render-target view, call <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a>.</li>
<li>To create a depth-stencil view, call <a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">ID3D10Device::CreateDepthStencilView</a>.</li>
<li>To create a shader-resource view, call <a href="https://msdn.microsoft.com/32e5d4d0-6686-4bcc-8ddb-fe519544051b">ID3D10Device::CreateShaderResourceView</a>.</li>
</ul>
All resources must be bound to the pipeline before they can be accessed.

<ul>
<li>To bind a render-target view or a depth-stencil view, call <a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">ID3D10Device::OMSetRenderTargets</a>.</li>
<li>To bind a shader-resource view, call <a href="https://msdn.microsoft.com/8481e388-3cfe-43e3-b58e-fea989d942ba">ID3D10Device::VSSetShaderResources</a>.</li>
</ul>
A view can also be used to access a <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">typeless resource</a>.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

