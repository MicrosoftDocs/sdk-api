---
UID: NN:d3d10.ID3D10DepthStencilView
title: ID3D10DepthStencilView (d3d10.h)
description: A depth-stencil-view interface accesses a texture resource during depth-stencil testing.helpviewer_keywords: ["ID3D10DepthStencilView","ID3D10DepthStencilView interface [Direct3D 10]","ID3D10DepthStencilView interface [Direct3D 10]","described","d3d10/ID3D10DepthStencilView","dac84102-a993-d10e-a776-72797e15d8c1","direct3d10.id3d10depthstencilview"]
old-location: direct3d10\id3d10depthstencilview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10depthstencilview.htm
ms.date: 12/05/2018
ms.keywords: ID3D10DepthStencilView, ID3D10DepthStencilView interface [Direct3D 10], ID3D10DepthStencilView interface [Direct3D 10],described, d3d10/ID3D10DepthStencilView, dac84102-a993-d10e-a776-72797e15d8c1, direct3d10.id3d10depthstencilview
f1_keywords:
- d3d10/ID3D10DepthStencilView
dev_langs:
- c++
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10DepthStencilView interface


## -description


A <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">depth-stencil-view</a> interface accesses a texture resource during  <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil testing</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10DepthStencilView</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>. <b>ID3D10DepthStencilView</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10depthstencilview-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a>.

</td>
</tr>
</table> 


## -remarks



To create a depth-stencil view, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>.

To bind a depth-stencil view to the pipeline, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">ID3D10Device::OMSetRenderTargets</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

