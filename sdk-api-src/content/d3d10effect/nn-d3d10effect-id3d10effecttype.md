---
UID: NN:d3d10effect.ID3D10EffectType
title: ID3D10EffectType
author: windows-driver-content
description: The ID3D10EffectType interface accesses effect variables by type.
old-location: direct3d10\id3d10effecttype.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttype.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10EffectType
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectType interface


## -description


The <b>ID3D10EffectType</b> interface accesses effect variables by type.

The lifetime of an <b>ID3D10EffectType</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a> object.
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
<a href="https://msdn.microsoft.com/cd046d58-8c7b-47b4-a75b-374edb06b33a">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect-type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9adddeb-5882-401f-92ef-72da5d7518f5">GetMemberName</a>
</td>
<td align="left" width="63%">
Get the name of a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88b471ad-d06e-43ef-b75e-a9528a0aef17">GetMemberSemantic</a>
</td>
<td align="left" width="63%">
Get the semantic attached to a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be109d28-1e7f-4500-ab7d-f450f34cb0d0">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a member type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c41503a-71d4-42c6-9a18-b2ff61edffcf">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get an member type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db483fb6-5d17-476d-8c6a-7d65eafd87f6">GetMemberTypeBySemantic</a>
</td>
<td align="left" width="63%">
Get a member type by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66a23a79-a381-45a9-9e2d-a8f68d698f51">IsValid</a>
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
<a href="https://msdn.microsoft.com/cd046d58-8c7b-47b4-a75b-374edb06b33a">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect-type description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9adddeb-5882-401f-92ef-72da5d7518f5">GetMemberName</a>
</td>
<td align="left" width="63%">
Get the name of a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88b471ad-d06e-43ef-b75e-a9528a0aef17">GetMemberSemantic</a>
</td>
<td align="left" width="63%">
Get the semantic attached to a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be109d28-1e7f-4500-ab7d-f450f34cb0d0">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a member type by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c41503a-71d4-42c6-9a18-b2ff61edffcf">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get an member type by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db483fb6-5d17-476d-8c6a-7d65eafd87f6">GetMemberTypeBySemantic</a>
</td>
<td align="left" width="63%">
Get a member type by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66a23a79-a381-45a9-9e2d-a8f68d698f51">IsValid</a>
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



To get information about an effect type from an effect variable, call <a href="https://msdn.microsoft.com/c1b081df-5cc6-45a2-860b-a214ef06f06a">ID3D10EffectVariable::GetType</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

