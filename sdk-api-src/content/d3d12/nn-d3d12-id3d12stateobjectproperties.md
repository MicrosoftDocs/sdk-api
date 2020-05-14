---
UID: NN:d3d12.ID3D12StateObjectProperties
title: ID3D12StateObjectProperties (d3d12.h)
description: Provides methods for getting and setting the properties of an ID3D12StateObject.helpviewer_keywords: ["ID3D12StateObjectProperties","ID3D12StateObjectProperties interface","ID3D12StateObjectProperties interface","described","d3d12/ID3D12StateObjectProperties","direct3d12.id3d12stateobjectproperties"]
old-location: direct3d12\id3d12stateobjectproperties.htm
tech.root: direct3d12
ms.assetid: 3971089A-2779-42FA-8FF9-6C7C8E39C7F9
ms.date: 12/05/2018
ms.keywords: ID3D12StateObjectProperties, ID3D12StateObjectProperties interface, ID3D12StateObjectProperties interface,described, d3d12/ID3D12StateObjectProperties, direct3d12.id3d12stateobjectproperties
f1_keywords:
- d3d12/ID3D12StateObjectProperties
dev_langs:
- c++
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D12.dll
api_name:
- ID3D12StateObjectProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12StateObjectProperties interface


## -description


Provides methods for getting and setting the properties of an <a href="https://msdn.microsoft.com/en-us/library/Mt815591(v=VS.85).aspx">ID3D12StateObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12StateObjectProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12StateObjectProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12StateObjectProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt815592(v=VS.85).aspx">GetPipelineStackSize</a>
</td>
<td align="left" width="63%">
Gets the current pipeline stack size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847467(v=VS.85).aspx">GetShaderIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier for a shader that can be used in a shader record.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847468(v=VS.85).aspx">GetShaderStackSize</a>
</td>
<td align="left" width="63%">
Gets the amount of stack memory required to invoke a raytracing shader in HLSL.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt815593(v=VS.85).aspx">SetPipelineStackSize</a>
</td>
<td align="left" width="63%">
Set the current pipeline stack size.  

</td>
</tr>
</table> 

