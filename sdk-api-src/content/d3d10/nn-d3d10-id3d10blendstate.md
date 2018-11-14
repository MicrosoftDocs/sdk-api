---
UID: NN:d3d10.ID3D10BlendState
title: ID3D10BlendState
author: windows-sdk-content
description: This blend-state interface accesses blending state for a Direct3D 10.0 device for the output-merger stage.
old-location: direct3d10\id3d10blendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blendstate.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10BlendState, ID3D10BlendState interface [Direct3D 10], ID3D10BlendState interface [Direct3D 10],described, d3d10/ID3D10BlendState, direct3d10.id3d10blendstate, e7edf841-099a-0302-cacb-da34c915ac4c
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
 - ID3D10BlendState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10BlendState interface


## -description


This blend-state interface accesses blending state for a Direct3D 10.0 device for the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger</a> stage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10BlendState</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10BlendState</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb173506(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the blend state.

</td>
</tr>
</table> 


## -remarks



Blending combines two pixel values. You have control over how the pixels are blended by using a predefined set of blending operations, as well as preblending operations. The <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">Blending Block Diagram</a> shows conceptually how blending works.

To create a blend-state interface, call <a href="https://msdn.microsoft.com/en-us/library/Bb173543(v=VS.85).aspx">ID3D10Device::CreateBlendState</a>. To initialize the blend state, call <a href="https://msdn.microsoft.com/en-us/library/Bb173595(v=VS.85).aspx">ID3D10Device::OMSetBlendState</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>
 

 

