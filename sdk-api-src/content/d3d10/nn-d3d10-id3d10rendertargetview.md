---
UID: NN:d3d10.ID3D10RenderTargetView
title: ID3D10RenderTargetView
author: windows-sdk-content
description: A render-target-view interface identifies the render-target subresources that can be accessed during rendering.
old-location: direct3d10\id3d10rendertargetview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10rendertargetview.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 76c9084d-ce0f-116d-42dd-eae6aa607d0e, ID3D10RenderTargetView, ID3D10RenderTargetView interface [Direct3D 10], ID3D10RenderTargetView interface [Direct3D 10],described, d3d10/ID3D10RenderTargetView, direct3d10.id3d10rendertargetview
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10RenderTargetView
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10RenderTargetView interface


## -description


A render-target-view interface identifies the render-target <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a> that can be accessed during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10RenderTargetView</b> interface inherits from <a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>. <b>ID3D10RenderTargetView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10RenderTargetView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e72220b-5798-4cdd-b749-b3cf56d94457">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a render target view.

</td>
</tr>
</table> 


## -remarks



To create a render-target view, call <a href="https://msdn.microsoft.com/950dc130-c23c-41e4-ad51-49167916fa5c">ID3D10Device::CreateRenderTargetView</a>. To bind a render-target view to the pipeline, call <a href="https://msdn.microsoft.com/68c20b1a-921a-4513-811b-f3b6999518f8">ID3D10Device::OMSetRenderTargets</a>.

A rendertarget is a resource that can be written by the output-merger stage at the end of a render pass. Each render-target should also have a corresponding depth-stencil view.




## -see-also




<a href="https://msdn.microsoft.com/a0b0945c-f907-4212-9bd5-a05033cdee45">ID3D10View</a>



<a href="https://msdn.microsoft.com/e53ca7ab-6ca5-4774-8a52-825b10c1a2ce">Resource Interfaces</a>
 

 

