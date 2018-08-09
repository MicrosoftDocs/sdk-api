---
UID: NN:d3d10effect.ID3D10EffectTechnique
title: ID3D10EffectTechnique
author: windows-sdk-content
description: An ID3D10EffectTechnique interface is a collection of passes.
old-location: direct3d10\id3d10effecttechnique.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 46580a58-26ee-e999-0d60-9585dc422459, ID3D10EffectTechnique, ID3D10EffectTechnique interface [Direct3D 10], ID3D10EffectTechnique interface [Direct3D 10],described, d3d10effect/ID3D10EffectTechnique, direct3d10.id3d10effecttechnique
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
 - ID3D10EffectTechnique
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectTechnique interface


## -description


An <b>ID3D10EffectTechnique</b> interface is a collection of passes.

The lifetime of an <b>ID3D10EffectTechnique</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a> object.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>ID3D10EffectTechnique</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173709(v=VS.85).aspx">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Compute a state-block mask to allow/prevent state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173710(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173711(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173712(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a technique description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173713(v=VS.85).aspx">GetPassByIndex</a>
</td>
<td align="left" width="63%">
Get a pass by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173714(v=VS.85).aspx">GetPassByName</a>
</td>
<td align="left" width="63%">
Get a pass by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173715(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Test a technique to see if it contains valid syntax.

</td>
</tr>
</table> 


## -members

The <b>ID3D10EffectTechnique</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173709(v=VS.85).aspx">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Compute a state-block mask to allow/prevent state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173710(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173711(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173712(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a technique description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173713(v=VS.85).aspx">GetPassByIndex</a>
</td>
<td align="left" width="63%">
Get a pass by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173714(v=VS.85).aspx">GetPassByName</a>
</td>
<td align="left" width="63%">
Get a pass by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173715(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Test a technique to see if it contains valid syntax.

</td>
</tr>
</table>Compute a state-block mask to allow/prevent state changes.

Get an annotation by index.

Get an annotation by name.

Get a technique description.

Get a pass by index.

Get a pass by name.

Test a technique to see if it contains valid syntax.

 


## -remarks



An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments (see <a href="https://msdn.microsoft.com/en-us/library/Bb205112(v=VS.85).aspx">Organizing State in an Effect (Direct3D 10)</a>). The syntax for creating a technique is shown in <a href="https://msdn.microsoft.com/en-us/library/Bb205053(v=VS.85).aspx">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-technique interface, call a method like <a href="https://msdn.microsoft.com/en-us/library/Bb173766(v=VS.85).aspx">ID3D10Effect::GetTechniqueByName</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>
 

 

