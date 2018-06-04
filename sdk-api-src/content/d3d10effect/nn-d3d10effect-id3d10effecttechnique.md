---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D10EffectTechnique interface


## -description


An <b>ID3D10EffectTechnique</b> interface is a collection of passes.

The lifetime of an <b>ID3D10EffectTechnique</b> object is equal to the lifetime of its parent <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a> object.
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
<a href="https://msdn.microsoft.com/c881dc2d-8e02-49b0-b539-bd0b1e767110">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Compute a state-block mask to allow/prevent state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6da71c9e-75b7-49dd-b9cb-871673e4b2c7">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0374cb3e-c609-4c39-9d68-9d189774022a">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18d53bb6-0055-479e-ac32-7f53498859c7">GetDesc</a>
</td>
<td align="left" width="63%">
Get a technique description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf7e4be-e25c-49ea-9851-db6a7415631a">GetPassByIndex</a>
</td>
<td align="left" width="63%">
Get a pass by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da96781-1233-47a0-a8b7-85acdb53ac49">GetPassByName</a>
</td>
<td align="left" width="63%">
Get a pass by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77001a77-04e9-40d9-8983-433e7513d3d5">IsValid</a>
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
<a href="https://msdn.microsoft.com/c881dc2d-8e02-49b0-b539-bd0b1e767110">ComputeStateBlockMask</a>
</td>
<td align="left" width="63%">
Compute a state-block mask to allow/prevent state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6da71c9e-75b7-49dd-b9cb-871673e4b2c7">GetAnnotationByIndex</a>
</td>
<td align="left" width="63%">
Get an annotation by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0374cb3e-c609-4c39-9d68-9d189774022a">GetAnnotationByName</a>
</td>
<td align="left" width="63%">
Get an annotation by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18d53bb6-0055-479e-ac32-7f53498859c7">GetDesc</a>
</td>
<td align="left" width="63%">
Get a technique description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf7e4be-e25c-49ea-9851-db6a7415631a">GetPassByIndex</a>
</td>
<td align="left" width="63%">
Get a pass by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da96781-1233-47a0-a8b7-85acdb53ac49">GetPassByName</a>
</td>
<td align="left" width="63%">
Get a pass by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77001a77-04e9-40d9-8983-433e7513d3d5">IsValid</a>
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



An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments (see <a href="https://msdn.microsoft.com/674ed278-102c-43da-a6bf-58e084df151e">Organizing State in an Effect (Direct3D 10)</a>). The syntax for creating a technique is shown in <a href="https://msdn.microsoft.com/84f9b74d-8397-4cd5-91a0-7f910ba7b19e">Effect Technique Syntax (Direct3D 10)</a>.

To get an effect-technique interface, call a method like <a href="https://msdn.microsoft.com/59c57254-f3e5-45a6-be3e-93bee67d5b36">ID3D10Effect::GetTechniqueByName</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

