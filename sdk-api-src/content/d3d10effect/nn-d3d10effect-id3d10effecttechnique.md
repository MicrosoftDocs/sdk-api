---
UID: NN:d3d10effect.ID3D10EffectTechnique
title: ID3D10EffectTechnique (d3d10effect.h)
description: An ID3D10EffectTechnique interface is a collection of passes.
helpviewer_keywords: ["46580a58-26ee-e999-0d60-9585dc422459","ID3D10EffectTechnique","ID3D10EffectTechnique interface [Direct3D 10]","ID3D10EffectTechnique interface [Direct3D 10]","described","d3d10effect/ID3D10EffectTechnique","direct3d10.id3d10effecttechnique"]
old-location: direct3d10\id3d10effecttechnique.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique.htm
ms.date: 12/05/2018
ms.keywords: 46580a58-26ee-e999-0d60-9585dc422459, ID3D10EffectTechnique, ID3D10EffectTechnique interface [Direct3D 10], ID3D10EffectTechnique interface [Direct3D 10],described, d3d10effect/ID3D10EffectTechnique, direct3d10.id3d10effecttechnique
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
 - ID3D10EffectTechnique
 - d3d10effect/ID3D10EffectTechnique
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
 - ID3D10EffectTechnique
---

# ID3D10EffectTechnique interface


## -description

An <b>ID3D10EffectTechnique</b> interface is a collection of passes.

The lifetime of an <b>ID3D10EffectTechnique</b> object is equal to the lifetime of its parent <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a> object.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-computestateblockmask">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Compute a state-block mask to allow/prevent state changes.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getannotationbyindex">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getannotationbyname">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a technique description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getpassbyindex">GetPassByIndex</a>
</td>
<td align="left" width="63%">
Get a pass by index.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getpassbyname">GetPassByName</a>
</td>
<td align="left" width="63%">
Get a pass by name.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-isvalid">IsValid</a>
</td>
<td align="left" width="63%">
Test a technique to see if it contains valid syntax.

</td>
</tr>
</table>

## -remarks

An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-organize">Organizing State in an Effect (Direct3D 10)</a>). The syntax for creating a technique is shown in <a href="/windows/desktop/direct3d10/d3d10-effect-technique-syntax">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-technique interface, call a method like <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-gettechniquebyname">ID3D10Effect::GetTechniqueByName</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>
