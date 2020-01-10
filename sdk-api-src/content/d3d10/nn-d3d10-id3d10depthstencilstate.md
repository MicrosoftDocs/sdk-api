---
UID: NN:d3d10.ID3D10DepthStencilState
title: ID3D10DepthStencilState (d3d10.h)
description: A depth-stencil-state interface accesses depth-stencil state which sets up the depth-stencil test for the output-merger stage.
old-location: direct3d10\id3d10depthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10depthstencilstate.htm
ms.date: 12/05/2018
ms.keywords: 756bea1e-80cb-6163-33a9-bbedb02e57da, ID3D10DepthStencilState, ID3D10DepthStencilState interface [Direct3D 10], ID3D10DepthStencilState interface [Direct3D 10],described, d3d10/ID3D10DepthStencilState, direct3d10.id3d10depthstencilstate
f1_keywords:
- d3d10/ID3D10DepthStencilState
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
- ID3D10DepthStencilState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10DepthStencilState interface


## -description


A depth-stencil-state interface accesses depth-stencil state which sets up the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil test</a> for the output-merger stage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10DepthStencilState</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10DepthStencilState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10DepthStencilState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10depthstencilstate-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil state.

</td>
</tr>
</table> 


## -remarks



Create a depth-stencil state object by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilstate">ID3D10Device::CreateDepthStencilState</a>.

To initialize depth-stencil state, bind the depth-stencil-state object to the pipeline by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetdepthstencilstate">ID3D10Device::OMSetDepthStencilState</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
 

 

