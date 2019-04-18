---
UID: NN:d3d10.ID3D10RasterizerState
title: ID3D10RasterizerState (d3d10.h)
author: windows-sdk-content
description: A rasterizer-state interface accesses rasterizer state for the rasterizer stage.
old-location: direct3d10\id3d10rasterizerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10rasterizerstate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10RasterizerState, ID3D10RasterizerState interface [Direct3D 10], ID3D10RasterizerState interface [Direct3D 10],described, ce1e96e6-707f-1c9e-1985-3b3acefd307f, d3d10/ID3D10RasterizerState, direct3d10.id3d10rasterizerstate
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
 - ID3D10RasterizerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10RasterizerState interface


## -description


A rasterizer-state interface accesses rasterizer state for the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10RasterizerState</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10RasterizerState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10RasterizerState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173826(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get the properties of a rasterizer-state object.

</td>
</tr>
</table> 


## -remarks



A rasterizer-state object is created with <a href="https://msdn.microsoft.com/en-us/library/Bb173554(v=VS.85).aspx">ID3D10Device::CreateRasterizerState</a> and bound to the pipeline with <a href="https://msdn.microsoft.com/en-us/library/Bb173612(v=VS.85).aspx">ID3D10Device::RSSetState</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>
 

 

