---
UID: NN:d3d10.ID3D10DepthStencilState
title: ID3D10DepthStencilState
author: windows-driver-content
description: A depth-stencil-state interface accesses depth-stencil state which sets up the depth-stencil test for the output-merger stage.
old-location: direct3d10\id3d10depthstencilstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10depthstencilstate.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 756bea1e-80cb-6163-33a9-bbedb02e57da, ID3D10DepthStencilState, ID3D10DepthStencilState interface [Direct3D 10], ID3D10DepthStencilState interface [Direct3D 10],described, d3d10/ID3D10DepthStencilState, direct3d10.id3d10depthstencilstate
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ID3D10DepthStencilState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DepthStencilState interface


## -description


A depth-stencil-state interface accesses depth-stencil state which sets up the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil test</a> for the output-merger stage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10DepthStencilState</b> interface inherits from <a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>. <b>ID3D10DepthStencilState</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/17e2aed6-0da6-494c-82c5-ba138255e0a1">GetDesc</a>
</td>
<td align="left" width="63%">
Get the depth-stencil state.

</td>
</tr>
</table> 


## -remarks



Create a depth-stencil state object by calling <a href="https://msdn.microsoft.com/41dab20f-53e7-488d-a0c5-7435122d81b8">ID3D10Device::CreateDepthStencilState</a>.

To initialize depth-stencil state, bind the depth-stencil-state object to the pipeline by calling <a href="https://msdn.microsoft.com/7cf8e5ca-08f2-4fa3-8657-cbce5d773dcf">ID3D10Device::OMSetDepthStencilState</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>
 

 

