---
UID: NN:d3d10.ID3D10DepthStencilView
title: ID3D10DepthStencilView
author: windows-sdk-content
description: A depth-stencil-view interface accesses a texture resource during depth-stencil testing.
old-location: direct3d10\id3d10depthstencilview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10depthstencilview.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D10DepthStencilView, ID3D10DepthStencilView interface [Direct3D 10], ID3D10DepthStencilView interface [Direct3D 10],described, d3d10/ID3D10DepthStencilView, dac84102-a993-d10e-a776-72797e15d8c1, direct3d10.id3d10depthstencilview
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10DepthStencilView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DepthStencilView interface


## -description


A <a href="https://msdn.microsoft.com/ccfe6273-0dcf-4b42-9d74-665a0b4cd14a">depth-stencil-view</a> interface accesses a texture resource during  <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil testing</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10DepthStencilView</b> interface inherits from <a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>. <b>ID3D10DepthStencilView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10DepthStencilView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2de1624-d971-47e9-aded-45add60bad93">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">view</a>.

</td>
</tr>
</table> 


## -remarks



To create a depth-stencil view, call <a href="https://msdn.microsoft.com/42bff154-36e6-4199-899c-c21917444c1d">ID3D10Device::CreateDepthStencilView</a>.

To bind a depth-stencil view to the pipeline, call <a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">ID3D10Device::OMSetRenderTargets</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

