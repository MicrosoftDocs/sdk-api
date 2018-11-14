---
UID: NN:d3d10effect.ID3D10EffectType
title: ID3D10EffectType
author: windows-sdk-content
description: The ID3D10EffectType interface accesses effect variables by type.
old-location: direct3d10\id3d10effecttype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttype.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 807ce993-4aee-8f2f-7837-5679d8a0dab0, ID3D10EffectType, ID3D10EffectType interface [Direct3D 10], ID3D10EffectType interface [Direct3D 10],described, d3d10effect/ID3D10EffectType, direct3d10.id3d10effecttype
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
 - ID3D10EffectType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectType interface


## -description


The <b>ID3D10EffectType</b> interface accesses effect variables by type.

The lifetime of an <b>ID3D10EffectType</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a> object.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>ID3D10EffectType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173717(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect-type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173718(v=VS.85).aspx">GetMemberName</a>
</td>
<td align="left" width="63%">
Get the name of a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173719(v=VS.85).aspx">GetMemberSemantic</a>
</td>
<td align="left" width="63%">
Get the semantic attached to a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173720(v=VS.85).aspx">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a member type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173721(v=VS.85).aspx">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get an member type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173722(v=VS.85).aspx">GetMemberTypeBySemantic</a>
</td>
<td align="left" width="63%">
Get a member type by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173723(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Tests that the effect type is valid.

</td>
</tr>
</table> 


## -members

The <b>ID3D10EffectType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173717(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect-type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173718(v=VS.85).aspx">GetMemberName</a>
</td>
<td align="left" width="63%">
Get the name of a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173719(v=VS.85).aspx">GetMemberSemantic</a>
</td>
<td align="left" width="63%">
Get the semantic attached to a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173720(v=VS.85).aspx">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a member type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173721(v=VS.85).aspx">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get an member type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173722(v=VS.85).aspx">GetMemberTypeBySemantic</a>
</td>
<td align="left" width="63%">
Get a member type by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173723(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Tests that the effect type is valid.

</td>
</tr>
</table>Get an effect-type description.

Get the name of a member.

Get the semantic attached to a member.

Get a member type by index.

Get an member type by name.

Get a member type by semantic.

Tests that the effect type is valid.

 


## -remarks



To get information about an effect type from an effect variable, call <a href="https://msdn.microsoft.com/en-us/library/Bb173745(v=VS.85).aspx">ID3D10EffectVariable::GetType</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>
 

 

