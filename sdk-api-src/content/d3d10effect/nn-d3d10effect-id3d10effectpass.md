---
UID: NN:d3d10effect.ID3D10EffectPass
title: ID3D10EffectPass (d3d10effect.h)
description: A pass interface encapsulates state assignments within a technique.
helpviewer_keywords: ["5cb1e1c5-e0ab-9620-8166-f4d77be0bd73","ID3D10EffectPass","ID3D10EffectPass interface [Direct3D 10]","ID3D10EffectPass interface [Direct3D 10]","described","d3d10effect/ID3D10EffectPass","direct3d10.id3d10effectpass"]
old-location: direct3d10\id3d10effectpass.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass.htm
ms.date: 12/05/2018
ms.keywords: 5cb1e1c5-e0ab-9620-8166-f4d77be0bd73, ID3D10EffectPass, ID3D10EffectPass interface [Direct3D 10], ID3D10EffectPass interface [Direct3D 10],described, d3d10effect/ID3D10EffectPass, direct3d10.id3d10effectpass
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
 - ID3D10EffectPass
 - d3d10effect/ID3D10EffectPass
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
 - ID3D10EffectPass
---

# ID3D10EffectPass interface


## -description

A pass interface encapsulates state assignments within a technique.

The lifetime of an <b>ID3D10EffectPass</b> object is equal to the lifetime of its parent <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect</a> object.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-apply">Apply</a>
</td>
<td align="left" width="63%">
Set the state contained in a pass to the device.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-computestateblockmask">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Generate a mask for allowing/preventing state changes.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getannotationbyindex">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getannotationbyname">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a pass description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getgeometryshaderdesc">GetGeometryShaderDesc</a>
</td>
<td align="left" width="63%">
Get a geometry-shader description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getpixelshaderdesc">GetPixelShaderDesc</a>
</td>
<td align="left" width="63%">
Get a pixel-shader description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getvertexshaderdesc">GetVertexShaderDesc</a>
</td>
<td align="left" width="63%">
Get a vertex-shader description.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-isvalid">IsValid</a>
</td>
<td align="left" width="63%">
Test a pass to see if it contains valid syntax.

</td>
</tr>
</table>

## -remarks

A pass is a block of code that sets render-state objects and shaders. A pass is declared within a technique; the syntax for a technique is shown in <a href="/windows/desktop/direct3d10/d3d10-effect-technique-syntax">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-pass interface, call a method like <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getpassbyname">ID3D10EffectTechnique::GetPassByName</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>
