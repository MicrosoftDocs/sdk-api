---
UID: NN:d3d10effect.ID3D10EffectVariable
title: ID3D10EffectVariable
author: windows-sdk-content
description: The ID3D10EffectVariable interface is the base class for all effect variables.
old-location: direct3d10\id3d10effectvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 8ca39e59-14b1-dd93-b1d0-8cf16752726e, ID3D10EffectVariable, ID3D10EffectVariable interface [Direct3D 10], ID3D10EffectVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectVariable, direct3d10.id3d10effectvariable
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
 - ID3D10EffectVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable interface


## -description


The <b>ID3D10EffectVariable</b> interface is the base class for all effect variables.

The lifetime of an <b>ID3D10EffectVariable</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a> object.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>ID3D10EffectVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173725(v=VS.85).aspx">AsBlend</a>
</td>
<td align="left" width="63%">
Get a effect-blend variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173726(v=VS.85).aspx">AsConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173727(v=VS.85).aspx">AsDepthStencil</a>
</td>
<td align="left" width="63%">
Get a depth-stencil variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb944007(v=VS.85).aspx">AsDepthStencilView</a>
</td>
<td align="left" width="63%">
Get a depth-stencil-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173728(v=VS.85).aspx">AsMatrix</a>
</td>
<td align="left" width="63%">
Get a matrix variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173729(v=VS.85).aspx">AsRasterizer</a>
</td>
<td align="left" width="63%">
Get a rasterizer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb944008(v=VS.85).aspx">AsRenderTargetView</a>
</td>
<td align="left" width="63%">
Get a render-target-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173730(v=VS.85).aspx">AsSampler</a>
</td>
<td align="left" width="63%">
Get a sampler variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173731(v=VS.85).aspx">AsScalar</a>
</td>
<td align="left" width="63%">
Get a scalar variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173732(v=VS.85).aspx">AsShader</a>
</td>
<td align="left" width="63%">
Get a shader variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173733(v=VS.85).aspx">AsShaderResource</a>
</td>
<td align="left" width="63%">
Get a shader-resource variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173734(v=VS.85).aspx">AsString</a>
</td>
<td align="left" width="63%">
Get a string variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173735(v=VS.85).aspx">AsVector</a>
</td>
<td align="left" width="63%">
Get a vector variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173736(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173737(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173738(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173739(v=VS.85).aspx">GetElement</a>
</td>
<td align="left" width="63%">
Get an array element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173740(v=VS.85).aspx">GetMemberByIndex</a>
</td>
<td align="left" width="63%">
Get a structure member by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173741(v=VS.85).aspx">GetMemberByName</a>
</td>
<td align="left" width="63%">
Get a structure member by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173742(v=VS.85).aspx">GetMemberBySemantic</a>
</td>
<td align="left" width="63%">
Get a structure member by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173743(v=VS.85).aspx">GetParentConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173744(v=VS.85).aspx">GetRawValue</a>
</td>
<td align="left" width="63%">
Get data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173745(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Get type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Compare the data type with the data stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173747(v=VS.85).aspx">SetRawValue</a>
</td>
<td align="left" width="63%">
Set data.

</td>
</tr>
</table> 


## -members

The <b>ID3D10EffectVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173725(v=VS.85).aspx">AsBlend</a>
</td>
<td align="left" width="63%">
Get a effect-blend variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173726(v=VS.85).aspx">AsConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173727(v=VS.85).aspx">AsDepthStencil</a>
</td>
<td align="left" width="63%">
Get a depth-stencil variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb944007(v=VS.85).aspx">AsDepthStencilView</a>
</td>
<td align="left" width="63%">
Get a depth-stencil-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173728(v=VS.85).aspx">AsMatrix</a>
</td>
<td align="left" width="63%">
Get a matrix variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173729(v=VS.85).aspx">AsRasterizer</a>
</td>
<td align="left" width="63%">
Get a rasterizer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb944008(v=VS.85).aspx">AsRenderTargetView</a>
</td>
<td align="left" width="63%">
Get a render-target-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173730(v=VS.85).aspx">AsSampler</a>
</td>
<td align="left" width="63%">
Get a sampler variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173731(v=VS.85).aspx">AsScalar</a>
</td>
<td align="left" width="63%">
Get a scalar variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173732(v=VS.85).aspx">AsShader</a>
</td>
<td align="left" width="63%">
Get a shader variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173733(v=VS.85).aspx">AsShaderResource</a>
</td>
<td align="left" width="63%">
Get a shader-resource variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173734(v=VS.85).aspx">AsString</a>
</td>
<td align="left" width="63%">
Get a string variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173735(v=VS.85).aspx">AsVector</a>
</td>
<td align="left" width="63%">
Get a vector variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173736(v=VS.85).aspx">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173737(v=VS.85).aspx">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173738(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173739(v=VS.85).aspx">GetElement</a>
</td>
<td align="left" width="63%">
Get an array element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173740(v=VS.85).aspx">GetMemberByIndex</a>
</td>
<td align="left" width="63%">
Get a structure member by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173741(v=VS.85).aspx">GetMemberByName</a>
</td>
<td align="left" width="63%">
Get a structure member by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173742(v=VS.85).aspx">GetMemberBySemantic</a>
</td>
<td align="left" width="63%">
Get a structure member by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173743(v=VS.85).aspx">GetParentConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173744(v=VS.85).aspx">GetRawValue</a>
</td>
<td align="left" width="63%">
Get data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173745(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Get type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Compare the data type with the data stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173747(v=VS.85).aspx">SetRawValue</a>
</td>
<td align="left" width="63%">
Set data.

</td>
</tr>
</table>Get a effect-blend variable.

Get a constant buffer.

Get a depth-stencil variable.

Get a depth-stencil-view variable.

Get a matrix variable.

Get a rasterizer variable.

Get a render-target-view variable.

Get a sampler variable.

Get a scalar variable.

Get a shader variable.

Get a shader-resource variable.

Get a string variable.

Get a vector variable.

Get an annotation by index.

Get an annotation by name.

Get a description.

Get an array element.

Get a structure member by index.

Get a structure member by name.

Get a structure member by semantic.

Get a constant buffer.

Get data.

Get type information.

Compare the data type with the data stored.

Set data.

 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>
 

 

