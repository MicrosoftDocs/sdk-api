---
UID: NN:d3d10effect.ID3D10EffectBlendVariable
title: ID3D10EffectBlendVariable
author: windows-sdk-content
description: The blend-variable interface accesses blend state.
old-location: direct3d10\id3d10effectblendvariable.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5dc3aa3a-6996-e7d4-76dc-917fe69d9260, ID3D10EffectBlendVariable, ID3D10EffectBlendVariable interface [Direct3D 10], ID3D10EffectBlendVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectBlendVariable, direct3d10.id3d10effectblendvariable
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10EffectBlendVariable
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectBlendVariable interface


## -description


The blend-variable interface accesses blend state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectBlendVariable</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>. <b>ID3D10EffectBlendVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectBlendVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173632(v=VS.85).aspx">GetBackingStore</a>
</td>
<td align="left" width="63%">
Get a pointer to a blend-state variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173633(v=VS.85).aspx">GetBlendState</a>
</td>
<td align="left" width="63%">
Get a pointer to a blend-state interface.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10EffectBlendVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="https://msdn.microsoft.com/library/Bb205115(v=VS.85).aspx">Two Ways to Get the State in an Effect Variable</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>
 

 

