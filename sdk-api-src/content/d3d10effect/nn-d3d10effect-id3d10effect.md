---
UID: NN:d3d10effect.ID3D10Effect
title: ID3D10Effect
author: windows-sdk-content
description: An ID3D10Effect interface manages a set of state objects, resources, and shaders for implementing a rendering effect.
old-location: direct3d10\id3d10effect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 8f18434d-7574-2504-c371-767566771aca, ID3D10Effect, ID3D10Effect interface [Direct3D 10], ID3D10Effect interface [Direct3D 10],described, d3d10effect/ID3D10Effect, direct3d10.id3d10effect
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Bb173761(v=VS.85).aspx">GetConstantBufferByIndex</a>
</td>
<td align="left" width="63%">
Get a constant buffer by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173762(v=VS.85).aspx">GetConstantBufferByName</a>
</td>
<td align="left" width="63%">
Get a constant buffer by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173763(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get an effect description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173764(v=VS.85).aspx">GetDevice</a>
</td>
<td align="left" width="63%">
Get the device that created the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173765(v=VS.85).aspx">GetTechniqueByIndex</a>
</td>
<td align="left" width="63%">
Get a technique by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173766(v=VS.85).aspx">GetTechniqueByName</a>
</td>
<td align="left" width="63%">
Get a technique by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173767(v=VS.85).aspx">GetVariableByIndex</a>
</td>
<td align="left" width="63%">
Get a variable by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173768(v=VS.85).aspx">GetVariableByName</a>
</td>
<td align="left" width="63%">
Get a variable by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173769(v=VS.85).aspx">GetVariableBySemantic</a>
</td>
<td align="left" width="63%">
Get a variable by semantic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173770(v=VS.85).aspx">IsOptimized</a>
</td>
<td align="left" width="63%">
Test an effect to see if the reflection metadata has been removed from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173771(v=VS.85).aspx">IsPool</a>
</td>
<td align="left" width="63%">
Test an effect to see if it is part of a memory pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173772(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Test an effect to see if it contains valid syntax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173773(v=VS.85).aspx">Optimize</a>
</td>
<td align="left" width="63%">
Minimize the amount of memory required for an effect.

</td>
</tr>
</table> 


## -remarks



An effect is created by calling <a href="https://msdn.microsoft.com/en-us/library/Bb205088(v=VS.85).aspx">D3D10CreateEffectFromMemory</a>.

The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb173327(v=VS.85).aspx">Effects (Direct3D 10)</a>.

<div class="alert"><b>Note</b>  <p class="note">If you call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an <b>ID3D10Effect</b> object to retrieve the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface, <b>QueryInterface</b> returns E_NOINTERFACE. To work around this issue, use the following code:


```
IUnknown* pIUnknown = (IUnknown*)pEffect;
    pIUnknown->AddRef();

```


</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205178(v=VS.85).aspx">Effect Interfaces (Direct3D 10)</a>
 

 

