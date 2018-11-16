---
UID: NN:d3d10effect.ID3D10EffectRasterizerVariable
title: ID3D10EffectRasterizerVariable
author: windows-sdk-content
description: A rasterizer-variable interface accesses rasterizer state.
old-location: direct3d10\id3d10effectrasterizervariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrasterizervariable.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D10EffectRasterizerVariable, ID3D10EffectRasterizerVariable interface [Direct3D 10], ID3D10EffectRasterizerVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectRasterizerVariable, direct3d10.id3d10effectrasterizervariable, e64c6162-c4a1-3cb0-6a8f-633ecb9840a6
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10EffectRasterizerVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectRasterizerVariable interface


## -description


A rasterizer-variable interface accesses rasterizer state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectRasterizerVariable</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>. <b>ID3D10EffectRasterizerVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectRasterizerVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173670(v=VS.85).aspx">GetBackingStore</a>
</td>
<td align="left" width="63%">
Get a pointer to a variable that contains rasteriser state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173671(v=VS.85).aspx">GetRasterizerState</a>
</td>
<td align="left" width="63%">
Get a pointer to a rasterizer interface.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10EffectRasterizerVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="https://msdn.microsoft.com/en-us/library/Bb205115(v=VS.85).aspx">Two Ways to Get the State in an Effect Variable</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>
 

 

