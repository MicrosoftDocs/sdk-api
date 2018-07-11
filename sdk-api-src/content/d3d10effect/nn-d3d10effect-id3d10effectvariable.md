---
UID: NN:d3d10effect.ID3D10EffectVariable
title: ID3D10EffectVariable
author: windows-sdk-content
description: The ID3D10EffectVariable interface is the base class for all effect variables.
old-location: direct3d10\id3d10effectvariable.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 8ca39e59-14b1-dd93-b1d0-8cf16752726e, ID3D10EffectVariable, ID3D10EffectVariable interface [Direct3D 10], ID3D10EffectVariable interface [Direct3D 10],described, d3d10effect/ID3D10EffectVariable, direct3d10.id3d10effectvariable
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
 - ID3D10EffectVariable
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10EffectVariable interface


## -description


The <b>ID3D10EffectVariable</b> interface is the base class for all effect variables.

The lifetime of an <b>ID3D10EffectVariable</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a> object.
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
<a href="https://msdn.microsoft.com/67400cd7-2253-4598-bc6c-8b45947ed2cb">AsBlend</a>
</td>
<td align="left" width="63%">
Get a effect-blend variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad172890-e6d1-4012-997f-5be45afedfad">AsConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39c23179-2fcf-44af-9091-6e3585c9fb79">AsDepthStencil</a>
</td>
<td align="left" width="63%">
Get a depth-stencil variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5ada392-1288-46e2-9b76-05d6d1938116">AsDepthStencilView</a>
</td>
<td align="left" width="63%">
Get a depth-stencil-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/234198b2-a42c-4a3e-a4f3-c79f268a4466">AsMatrix</a>
</td>
<td align="left" width="63%">
Get a matrix variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/927ebdfc-6029-4c23-806a-185ffd9f303b">AsRasterizer</a>
</td>
<td align="left" width="63%">
Get a rasterizer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b91110f-7430-4300-af58-da2af08209f7">AsRenderTargetView</a>
</td>
<td align="left" width="63%">
Get a render-target-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe0d693-f6df-4163-b22f-b06495cc2c8e">AsSampler</a>
</td>
<td align="left" width="63%">
Get a sampler variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af1cdd1-4f04-4568-8494-d1be83d34267">AsScalar</a>
</td>
<td align="left" width="63%">
Get a scalar variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13e2b5c5-b959-4a9c-8a19-809b8a3bcd48">AsShader</a>
</td>
<td align="left" width="63%">
Get a shader variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d861dcb-2350-49f1-bb0f-28a28ebfd131">AsShaderResource</a>
</td>
<td align="left" width="63%">
Get a shader-resource variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3ef95f7-7a12-4786-9010-d8d8aef5a33c">AsString</a>
</td>
<td align="left" width="63%">
Get a string variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a10128fd-143a-4d69-a32d-a7756eb62c89">AsVector</a>
</td>
<td align="left" width="63%">
Get a vector variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/793e3524-0d16-467c-ae0a-bd6cba11e4e3">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39776686-ef51-48dc-a408-45ca934b7119">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64ab5d84-834b-49cf-a873-6c249d808662">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8be279d0-834d-4eca-9c34-eadcd9c32ace">GetElement</a>
</td>
<td align="left" width="63%">
Get an array element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48aee944-7ae9-4d2e-acf8-1f33a3ce05e1">GetMemberByIndex</a>
</td>
<td align="left" width="63%">
Get a structure member by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42a57e27-0a6c-4612-ae1f-04754c5320c2">GetMemberByName</a>
</td>
<td align="left" width="63%">
Get a structure member by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4000c9e9-4648-4a23-8964-658479db83fc">GetMemberBySemantic</a>
</td>
<td align="left" width="63%">
Get a structure member by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf23c3fc-e42e-451b-b53a-1e5888fef6b3">GetParentConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e748d6d7-fb39-44bd-b532-9e631370e8dd">GetRawValue</a>
</td>
<td align="left" width="63%">
Get data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Get type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>
</td>
<td align="left" width="63%">
Compare the data type with the data stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14fb6d74-39a4-4f79-8fdc-c25d96be1531">SetRawValue</a>
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
<a href="https://msdn.microsoft.com/67400cd7-2253-4598-bc6c-8b45947ed2cb">AsBlend</a>
</td>
<td align="left" width="63%">
Get a effect-blend variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad172890-e6d1-4012-997f-5be45afedfad">AsConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39c23179-2fcf-44af-9091-6e3585c9fb79">AsDepthStencil</a>
</td>
<td align="left" width="63%">
Get a depth-stencil variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5ada392-1288-46e2-9b76-05d6d1938116">AsDepthStencilView</a>
</td>
<td align="left" width="63%">
Get a depth-stencil-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/234198b2-a42c-4a3e-a4f3-c79f268a4466">AsMatrix</a>
</td>
<td align="left" width="63%">
Get a matrix variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/927ebdfc-6029-4c23-806a-185ffd9f303b">AsRasterizer</a>
</td>
<td align="left" width="63%">
Get a rasterizer variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b91110f-7430-4300-af58-da2af08209f7">AsRenderTargetView</a>
</td>
<td align="left" width="63%">
Get a render-target-view variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe0d693-f6df-4163-b22f-b06495cc2c8e">AsSampler</a>
</td>
<td align="left" width="63%">
Get a sampler variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af1cdd1-4f04-4568-8494-d1be83d34267">AsScalar</a>
</td>
<td align="left" width="63%">
Get a scalar variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13e2b5c5-b959-4a9c-8a19-809b8a3bcd48">AsShader</a>
</td>
<td align="left" width="63%">
Get a shader variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d861dcb-2350-49f1-bb0f-28a28ebfd131">AsShaderResource</a>
</td>
<td align="left" width="63%">
Get a shader-resource variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3ef95f7-7a12-4786-9010-d8d8aef5a33c">AsString</a>
</td>
<td align="left" width="63%">
Get a string variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a10128fd-143a-4d69-a32d-a7756eb62c89">AsVector</a>
</td>
<td align="left" width="63%">
Get a vector variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/793e3524-0d16-467c-ae0a-bd6cba11e4e3">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39776686-ef51-48dc-a408-45ca934b7119">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64ab5d84-834b-49cf-a873-6c249d808662">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8be279d0-834d-4eca-9c34-eadcd9c32ace">GetElement</a>
</td>
<td align="left" width="63%">
Get an array element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48aee944-7ae9-4d2e-acf8-1f33a3ce05e1">GetMemberByIndex</a>
</td>
<td align="left" width="63%">
Get a structure member by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42a57e27-0a6c-4612-ae1f-04754c5320c2">GetMemberByName</a>
</td>
<td align="left" width="63%">
Get a structure member by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4000c9e9-4648-4a23-8964-658479db83fc">GetMemberBySemantic</a>
</td>
<td align="left" width="63%">
Get a structure member by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf23c3fc-e42e-451b-b53a-1e5888fef6b3">GetParentConstantBuffer</a>
</td>
<td align="left" width="63%">
Get a constant buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e748d6d7-fb39-44bd-b532-9e631370e8dd">GetRawValue</a>
</td>
<td align="left" width="63%">
Get data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Get type information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>
</td>
<td align="left" width="63%">
Compare the data type with the data stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14fb6d74-39a4-4f79-8fdc-c25d96be1531">SetRawValue</a>
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




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

