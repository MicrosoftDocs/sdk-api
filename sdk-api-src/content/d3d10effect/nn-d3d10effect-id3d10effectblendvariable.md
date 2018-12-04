---
UID: NN:d3d10effect.ID3D10EffectBlendVariable
title: ID3D10EffectBlendVariable
author: windows-sdk-content
description: The blend-variable interface accesses blend state.
old-location: direct3d10\id3d10effectblendvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectblendvariable.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 5dc3aa3a-6996-e7d4-76dc-917fe69d9260, ID3D10EffectBlendVariable, ID3D10EffectBlendVariable interface [Direct3D 10], ID3D10EffectBlendVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectBlendVariable, direct3d10.id3d10effectblendvariable
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
 - ID3D10EffectBlendVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectBlendVariable interface


## -description


The blend-variable interface accesses blend state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectBlendVariable</b> interface inherits from <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>. <b>ID3D10EffectBlendVariable</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6252c7b2-60c9-42c3-8d51-71c59b02dfc1">GetBackingStore</a>
</td>
<td align="left" width="63%">
Get a pointer to a blend-state variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48261026-6990-45db-a6f6-1cb30671c4a0">GetBlendState</a>
</td>
<td align="left" width="63%">
Get a pointer to a blend-state interface.

</td>
</tr>
</table> 


## -remarks



An <b>ID3D10EffectBlendVariable Interface</b> is created when an effect is read into memory.

Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. You
 can use either of these methods to return state. For examples, see <a href="https://msdn.microsoft.com/743261a8-fdd8-492e-be8a-4faeb9b6f986">Two Ways to Get the State in an Effect Variable</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>



<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>
 

 

