---
UID: NN:d3d10effect.ID3D10EffectDepthStencilVariable
title: ID3D10EffectDepthStencilVariable
author: windows-sdk-content
description: A depth-stencil-variable interface accesses depth-stencil state.
old-location: direct3d10\id3d10effectdepthstencilvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilvariable.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 896bf0ca-5516-5a5a-b85d-a24c6e618bc1, ID3D10EffectDepthStencilVariable, ID3D10EffectDepthStencilVariable interface [Direct3D 10], ID3D10EffectDepthStencilVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectDepthStencilVariable, direct3d10.id3d10effectdepthstencilvariable
ms.topic: interface
req.header: d3d10effect.h
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
 - ID3D10EffectDepthStencilVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectDepthStencilVariable interface


## -description


A depth-stencil-variable interface accesses depth-stencil state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectDepthStencilVariable</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>. <b>ID3D10EffectDepthStencilVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectDepthStencilVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173640(v=VS.85).aspx">GetBackingStore</a>
</td>
<td align="left" width="63%">
Get a pointer to a variable that contains depth-stencil state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173641(v=VS.85).aspx">GetDepthStencilState</a>
</td>
<td align="left" width="63%">
Get a pointer to a depth-stencil interface.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10EffectDepthStencilVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="https://msdn.microsoft.com/en-us/library/Bb205115(v=VS.85).aspx">Two Ways to Get the State in an Effect Variable</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>
 

 

