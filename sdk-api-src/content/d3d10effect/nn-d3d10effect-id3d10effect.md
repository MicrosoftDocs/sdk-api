---
UID: NN:d3d10effect.ID3D10Effect
title: ID3D10Effect
author: windows-driver-content
description: An ID3D10Effect interface manages a set of state objects, resources, and shaders for implementing a rendering effect.
old-location: direct3d10\id3d10effect.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 8f18434d-7574-2504-c371-767566771aca, ID3D10Effect, ID3D10Effect interface [Direct3D 10], ID3D10Effect interface [Direct3D 10],described, d3d10effect/ID3D10Effect, direct3d10.id3d10effect
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Effect
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Effect interface


## -description


An <b>ID3D10Effect</b> interface manages a set of state objects, resources, and shaders for implementing a rendering effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Effect</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Effect</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/184e9640-98f9-4909-8c36-d25306716ee8">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/020a5535-f606-443e-bc58-0d37aa0e933f">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc8add27-778b-416e-a031-d5861ec79b90">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Get the device that created the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86048fc8-c610-4fd2-aff7-604cd3c3c836">GetTechniqueByIndex</a>
</td>
<td align="left" width="63%">
Get a technique by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59c57254-f3e5-45a6-be3e-93bee67d5b36">GetTechniqueByName</a>
</td>
<td align="left" width="63%">
Get a technique by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a85731c-8c79-4428-9047-f20436962d1e">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Get a variable by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3636896-c472-4d94-9cc5-5eabba40fabb">GetVariableByName</a>
</td>
<td align="left" width="63%">
Get a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed7272b2-b170-4044-8662-aadab360e845">GetVariableBySemantic</a>
</td>
<td align="left" width="63%">
Get a variable by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b12ebb2b-0a47-41cf-80d8-29575a3ca30e">IsOptimized</a>
</td>
<td align="left" width="63%">
Test an effect to see if the reflection metadata has been removed from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0afbeba0-4010-4114-8d0f-007d92a78f41">IsPool</a>
</td>
<td align="left" width="63%">
Test an effect to see if it is part of a memory pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e31defc8-92cf-4409-bfe6-5e8e98c4e44f">IsValid</a>
</td>
<td align="left" width="63%">
Test an effect to see if it contains valid syntax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73e61b9c-d1da-4e1a-961c-5916c96bdc42">Optimize</a>
</td>
<td align="left" width="63%">
Minimize the amount of memory required for an effect.

</td>
</tr>
</table> 


## -remarks



An effect is created by calling <a href="https://msdn.microsoft.com/0852b937-283f-496f-8a32-4f9a0d769572">D3D10CreateEffectFromMemory</a>.

The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders. For more information, see <a href="https://msdn.microsoft.com/db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e">Effects (Direct3D 10)</a>.

<div class="alert"><b>Note</b>  <p class="note">If you call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an <b>ID3D10Effect</b> object to retrieve the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface, <b>QueryInterface</b> returns E_NOINTERFACE. To work around this issue, use the following code:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    IUnknown* pIUnknown = (IUnknown*)pEffect;
    pIUnknown-&gt;AddRef();
</pre>
</td>
</tr>
</table></span></div>
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ebe0afc7-6261-4c96-a54e-9b491e240c03">Effect Interfaces (Direct3D 10)</a>
 

 

