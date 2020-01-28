---
UID: NN:d3d10effect.ID3D10Effect
title: ID3D10Effect (d3d10effect.h)
description: An ID3D10Effect interface manages a set of state objects, resources, and shaders for implementing a rendering effect.
old-location: direct3d10\id3d10effect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect.htm
ms.date: 12/05/2018
ms.keywords: 8f18434d-7574-2504-c371-767566771aca, ID3D10Effect, ID3D10Effect interface [Direct3D 10], ID3D10Effect interface [Direct3D 10],described, d3d10effect/ID3D10Effect, direct3d10.id3d10effect
f1_keywords:
- d3d10effect/ID3D10Effect
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
- ID3D10Effect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Effect interface


## -description


An <b>ID3D10Effect</b> interface manages a set of state objects, resources, and shaders for implementing a rendering effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Effect</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Effect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Effect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getconstantbufferbyindex">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getconstantbufferbyname">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Get the device that created the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-gettechniquebyindex">GetTechniqueByIndex</a>
</td>
<td align="left" width="63%">
Get a technique by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-gettechniquebyname">GetTechniqueByName</a>
</td>
<td align="left" width="63%">
Get a technique by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebyindex">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Get a variable by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebyname">GetVariableByName</a>
</td>
<td align="left" width="63%">
Get a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getvariablebysemantic">GetVariableBySemantic</a>
</td>
<td align="left" width="63%">
Get a variable by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-isoptimized">IsOptimized</a>
</td>
<td align="left" width="63%">
Test an effect to see if the reflection metadata has been removed from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-ispool">IsPool</a>
</td>
<td align="left" width="63%">
Test an effect to see if it is part of a memory pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-isvalid">IsValid</a>
</td>
<td align="left" width="63%">
Test an effect to see if it contains valid syntax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-optimize">Optimize</a>
</td>
<td align="left" width="63%">
Minimize the amount of memory required for an effect.

</td>
</tr>
</table> 


## -remarks



An effect is created by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-d3d10createeffectfrommemory">D3D10CreateEffectFromMemory</a>.

The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders. For more information, see <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects">Effects (Direct3D 10)</a>.

<div class="alert"><b>Note</b>  <p class="note">If you call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an <b>ID3D10Effect</b> object to retrieve the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface, <b>QueryInterface</b> returns E_NOINTERFACE. To work around this issue, use the following code:


```
IUnknown* pIUnknown = (IUnknown*)pEffect;
    pIUnknown->AddRef();

```


</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>
 

 

