---
UID: NN:d3d10effect.ID3D10EffectPass
title: ID3D10EffectPass
author: windows-sdk-content
description: A pass interface encapsulates state assignments within a technique.
old-location: direct3d10\id3d10effectpass.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5cb1e1c5-e0ab-9620-8166-f4d77be0bd73, ID3D10EffectPass, ID3D10EffectPass interface [Direct3D 10], ID3D10EffectPass interface [Direct3D 10],described, d3d10effect/ID3D10EffectPass, direct3d10.id3d10effectpass
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
 - ID3D10EffectPass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectPass interface


## -description


A pass interface encapsulates state assignments within a technique.

The lifetime of an <b>ID3D10EffectPass</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a> object.
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
<a href="https://msdn.microsoft.com/00876091-0893-4370-816e-a8c367f430a7">Apply</a>
</td>
<td align="left" width="63%">
Set the state contained in a pass to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab4ad7b6-ad6a-44b5-bb07-42b7b92b3f1b">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Generate a mask for allowing/preventing state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3476787-502a-4b02-be92-c541324cbb86">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5669175c-c199-45b1-81fd-5adf6760565b">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40744216-0199-4667-a4ad-69a56811b52c">GetDesc</a>
</td>
<td align="left" width="63%">
Get a pass description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e52466f8-d38a-4306-b2c5-a0446b596970">GetGeometryShaderDesc</a>
</td>
<td align="left" width="63%">
Get a geometry-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6706a4bc-080c-4a5a-8517-70cca6358298">GetPixelShaderDesc</a>
</td>
<td align="left" width="63%">
Get a pixel-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a213647-66b8-4beb-8f08-cc45bc361116">GetVertexShaderDesc</a>
</td>
<td align="left" width="63%">
Get a vertex-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0dce5c6-c8f7-4745-8e89-993bb7e5ff8e">IsValid</a>
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
<a href="https://msdn.microsoft.com/00876091-0893-4370-816e-a8c367f430a7">Apply</a>
</td>
<td align="left" width="63%">
Set the state contained in a pass to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab4ad7b6-ad6a-44b5-bb07-42b7b92b3f1b">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Generate a mask for allowing/preventing state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3476787-502a-4b02-be92-c541324cbb86">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5669175c-c199-45b1-81fd-5adf6760565b">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40744216-0199-4667-a4ad-69a56811b52c">GetDesc</a>
</td>
<td align="left" width="63%">
Get a pass description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e52466f8-d38a-4306-b2c5-a0446b596970">GetGeometryShaderDesc</a>
</td>
<td align="left" width="63%">
Get a geometry-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6706a4bc-080c-4a5a-8517-70cca6358298">GetPixelShaderDesc</a>
</td>
<td align="left" width="63%">
Get a pixel-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a213647-66b8-4beb-8f08-cc45bc361116">GetVertexShaderDesc</a>
</td>
<td align="left" width="63%">
Get a vertex-shader description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0dce5c6-c8f7-4745-8e89-993bb7e5ff8e">IsValid</a>
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



A pass is a block of code that sets render-state objects and shaders. A pass is declared within a technique; the syntax for a technique is shown in <a href="https://msdn.microsoft.com/84f9b74d-8397-4cd5-91a0-7f910ba7b19e">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-pass interface, call a method like <a href="https://msdn.microsoft.com/9da96781-1233-47a0-a8b7-85acdb53ac49">ID3D10EffectTechnique::GetPassByName</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

