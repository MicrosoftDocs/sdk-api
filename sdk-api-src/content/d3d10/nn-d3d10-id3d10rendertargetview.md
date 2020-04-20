---
UID: NN:d3d10.ID3D10RenderTargetView
title: ID3D10RenderTargetView (d3d10.h)
description: A render-target-view interface identifies the render-target subresources that can be accessed during rendering.helpviewer_keywords: ["76c9084d-ce0f-116d-42dd-eae6aa607d0e","ID3D10RenderTargetView","ID3D10RenderTargetView interface [Direct3D 10]","ID3D10RenderTargetView interface [Direct3D 10]","described","d3d10/ID3D10RenderTargetView","direct3d10.id3d10rendertargetview"]
old-location: direct3d10\id3d10rendertargetview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10rendertargetview.htm
ms.date: 12/05/2018
ms.keywords: 76c9084d-ce0f-116d-42dd-eae6aa607d0e, ID3D10RenderTargetView, ID3D10RenderTargetView interface [Direct3D 10], ID3D10RenderTargetView interface [Direct3D 10],described, d3d10/ID3D10RenderTargetView, direct3d10.id3d10rendertargetview
f1_keywords:
- d3d10/ID3D10RenderTargetView
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
- ID3D10RenderTargetView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10RenderTargetView interface


## -description


A render-target-view interface identifies the render-target <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresources</a> that can be accessed during rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10RenderTargetView</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>. <b>ID3D10RenderTargetView</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10rendertargetview-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a render target view.

</td>
</tr>
</table> 


## -remarks



To create a render-target view, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>. To bind a render-target view to the pipeline, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">ID3D10Device::OMSetRenderTargets</a>.

A rendertarget is a resource that can be written by the output-merger stage at the end of a render pass. Each render-target should also have a corresponding depth-stencil view.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10view">ID3D10View</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
 

 

