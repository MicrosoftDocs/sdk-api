---
UID: NN:d3d10effect.ID3D10EffectType
title: ID3D10EffectType (d3d10effect.h)
description: The ID3D10EffectType interface accesses effect variables by type.
helpviewer_keywords: ["807ce993-4aee-8f2f-7837-5679d8a0dab0","ID3D10EffectType","ID3D10EffectType interface [Direct3D 10]","ID3D10EffectType interface [Direct3D 10]","described","d3d10effect/ID3D10EffectType","direct3d10.id3d10effecttype"]
old-location: direct3d10\id3d10effecttype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttype.htm
ms.date: 12/05/2018
ms.keywords: 807ce993-4aee-8f2f-7837-5679d8a0dab0, ID3D10EffectType, ID3D10EffectType interface [Direct3D 10], ID3D10EffectType interface [Direct3D 10],described, d3d10effect/ID3D10EffectType, direct3d10.id3d10effecttype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectType
 - d3d10effect/ID3D10EffectType
dev_langs:
 - c++
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
---

# ID3D10EffectType interface


## -description

The <b>ID3D10EffectType</b> interface accesses effect variables by type.

The lifetime of an <b>ID3D10EffectType</b> object is equal to the lifetime of its parent <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a> object.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect-type description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getmembername">GetMemberName</a>
</td>
<td align="left" width="63%">
Get the name of a member.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getmembersemantic">GetMemberSemantic</a>
</td>
<td align="left" width="63%">
Get the semantic attached to a member.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getmembertypebyindex">GetMemberTypeByIndex</a>
</td>
<td align="left" width="63%">
Get a member type by index.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getmembertypebyname">GetMemberTypeByName</a>
</td>
<td align="left" width="63%">
Get a member type by name.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-getmembertypebysemantic">GetMemberTypeBySemantic</a>
</td>
<td align="left" width="63%">
Get a member type by semantic.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttype-isvalid">IsValid</a>
</td>
<td align="left" width="63%">
Tests that the effect type is valid.

</td>
</tr>
</table>

## -remarks

To get information about an effect type from an effect variable, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-gettype">ID3D10EffectVariable::GetType</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>
