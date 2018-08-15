---
UID: NN:d3d10effect.ID3D10EffectPass
title: ID3D10EffectPass
author: windows-sdk-content
description: A pass interface encapsulates state assignments within a technique.
old-location: direct3d10\id3d10effectpass.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 5cb1e1c5-e0ab-9620-8166-f4d77be0bd73, ID3D10EffectPass, ID3D10EffectPass interface [Direct3D 10], ID3D10EffectPass interface [Direct3D 10],described, d3d10effect/ID3D10EffectPass, direct3d10.id3d10effectpass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
 - ID3D10EffectPass
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectPass interface


## -description


A pass interface encapsulates state assignments within a technique.

The lifetime of an <b>ID3D10EffectPass</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a> object.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>ID3D10EffectPass</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173657(v=VS.85).aspx">Apply</a>
</td>
<td align="left" width="63%">
Set the state contained in a pass to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173658(v=VS.85).aspx">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Generate a mask for allowing/preventing state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173659(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173660(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173661(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a pass description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173662(v=VS.85).aspx">GetGeometryShaderDesc</a>
</td>
<td align="left" width="63%">
Get a geometry-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173663(v=VS.85).aspx">GetPixelShaderDesc</a>
</td>
<td align="left" width="63%">
Get a pixel-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173664(v=VS.85).aspx">GetVertexShaderDesc</a>
</td>
<td align="left" width="63%">
Get a vertex-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173665(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Test a pass to see if it contains valid syntax.

</td>
</tr>
</table> 


## -members

The <b>ID3D10EffectPass</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173657(v=VS.85).aspx">Apply</a>
</td>
<td align="left" width="63%">
Set the state contained in a pass to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173658(v=VS.85).aspx">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Generate a mask for allowing/preventing state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173659(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173660(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173661(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a pass description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173662(v=VS.85).aspx">GetGeometryShaderDesc</a>
</td>
<td align="left" width="63%">
Get a geometry-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173663(v=VS.85).aspx">GetPixelShaderDesc</a>
</td>
<td align="left" width="63%">
Get a pixel-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173664(v=VS.85).aspx">GetVertexShaderDesc</a>
</td>
<td align="left" width="63%">
Get a vertex-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173665(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Test a pass to see if it contains valid syntax.

</td>
</tr>
</table>Set the state contained in a pass to the device.

Generate a mask for allowing/preventing state changes.

Get an annotation by index.

Get an annotation by name.

Get a pass description.

Get a geometry-shader description.

Get a pixel-shader description.

Get a vertex-shader description.

Test a pass to see if it contains valid syntax.

 


## -remarks



A pass is a block of code that sets render-state objects and shaders. A pass is declared within a technique; the syntax for a technique is shown in <a href="https://msdn.microsoft.com/en-us/library/Bb205053(v=VS.85).aspx">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-pass interface, call a method like <a href="https://msdn.microsoft.com/en-us/library/Bb173714(v=VS.85).aspx">ID3D10EffectTechnique::GetPassByName</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>
 

 

