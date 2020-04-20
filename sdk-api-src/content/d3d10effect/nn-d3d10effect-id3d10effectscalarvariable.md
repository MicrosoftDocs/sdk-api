---
UID: NN:d3d10effect.ID3D10EffectScalarVariable
title: ID3D10EffectScalarVariable (d3d10effect.h)
description: An effect-scalar-variable interface accesses scalar values.helpviewer_keywords: ["0954ac9f-acd1-fb91-e361-0b5644656816","ID3D10EffectScalarVariable","ID3D10EffectScalarVariable interface [Direct3D 10]","ID3D10EffectScalarVariable interface [Direct3D 10]","described","d3d10effect/ID3D10EffectScalarVariable","direct3d10.id3d10effectscalarvariable"]
old-location: direct3d10\id3d10effectscalarvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable.htm
ms.date: 12/05/2018
ms.keywords: 0954ac9f-acd1-fb91-e361-0b5644656816, ID3D10EffectScalarVariable, ID3D10EffectScalarVariable interface [Direct3D 10], ID3D10EffectScalarVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectScalarVariable, direct3d10.id3d10effectscalarvariable
f1_keywords:
- d3d10effect/ID3D10EffectScalarVariable
dev_langs:
- c++
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
- ID3D10EffectScalarVariable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectScalarVariable interface


## -description


An effect-scalar-variable interface accesses scalar values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10EffectScalarVariable</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>. <b>ID3D10EffectScalarVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10EffectScalarVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getbool">GetBool</a>
</td>
<td align="left" width="63%">
Get a boolean variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getboolarray">GetBoolArray</a>
</td>
<td align="left" width="63%">
Get an array of boolean variables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getfloat">GetFloat</a>
</td>
<td align="left" width="63%">
Get a floating-point variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getfloatarray">GetFloatArray</a>
</td>
<td align="left" width="63%">
Get an array of floating-point variables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getint">GetInt</a>
</td>
<td align="left" width="63%">
Get an integer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-getintarray">GetIntArray</a>
</td>
<td align="left" width="63%">
Get an array of integer variables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setbool">SetBool</a>
</td>
<td align="left" width="63%">
Set a boolean variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setboolarray">SetBoolArray</a>
</td>
<td align="left" width="63%">
Set an array of boolean variables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setfloat">SetFloat</a>
</td>
<td align="left" width="63%">
Set a floating-point variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setfloatarray">SetFloatArray</a>
</td>
<td align="left" width="63%">
Set an array of floating-point variables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setint">SetInt</a>
</td>
<td align="left" width="63%">
Set an integer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectscalarvariable-setintarray">SetIntArray</a>
</td>
<td align="left" width="63%">
Set an array of integer variables.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>
 

 

