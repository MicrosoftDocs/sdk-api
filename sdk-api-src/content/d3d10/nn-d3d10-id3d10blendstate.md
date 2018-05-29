---
UID: NN:d3d10.ID3D10BlendState
title: ID3D10BlendState
author: windows-sdk-content
description: This blend-state interface accesses blending state for a Direct3D 10.0 device for the output-merger stage.
old-location: direct3d10\id3d10blendstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blendstate.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10BlendState, ID3D10BlendState interface [Direct3D 10], ID3D10BlendState interface [Direct3D 10],described, d3d10/ID3D10BlendState, direct3d10.id3d10blendstate, e7edf841-099a-0302-cacb-da34c915ac4c
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
-	ID3D10BlendState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10BlendState interface


## -description


This blend-state interface accesses blending state for a Direct3D 10.0 device for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger</a> stage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10BlendState</b> interface inherits from <a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>. <b>ID3D10BlendState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10BlendState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c35544f-437e-4532-937e-c521b6a30e49">GetDesc</a>
</td>
<td align="left" width="63%">
Get the blend state.

</td>
</tr>
</table> 


## -remarks



Blending combines two pixel values. You have control over how the pixels are blended by using a predefined set of blending operations, as well as preblending operations. The <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">Blending Block Diagram</a> shows conceptually how blending works.

To create a blend-state interface, call <a href="https://msdn.microsoft.com/4a5b000d-769b-4e4c-9c9c-d8fced703812">ID3D10Device::CreateBlendState</a>. To initialize the blend state, call <a href="https://msdn.microsoft.com/39169f4f-8a7b-4db0-abd5-5b67b204b394">ID3D10Device::OMSetBlendState</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>



<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>
 

 

