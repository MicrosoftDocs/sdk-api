---
UID: NN:d3d12.ID3D12StateObjectProperties
title: ID3D12StateObjectProperties
author: windows-sdk-content
description: Provides methods for getting and setting the properties of an ID3D12StateObject.
old-location: direct3d12\id3d12stateobjectproperties.htm
tech.root: direct3d12
ms.assetid: 3971089A-2779-42FA-8FF9-6C7C8E39C7F9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12StateObjectProperties, ID3D12StateObjectProperties interface, ID3D12StateObjectProperties interface,described, d3d12/ID3D12StateObjectProperties, direct3d12.id3d12stateobjectproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12StateObjectProperties interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Provides methods for getting and setting the properties of an <a href="https://msdn.microsoft.com/5BE94583-31DC-4469-9049-7768D64F7F41">ID3D12StateObject</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12StateObjectProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12StateObjectProperties</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6570D84B-F589-4090-8F08-F91B12B0E283">GetPipelineStackSize</a>
</td>
<td align="left" width="63%">
Gets the current pipeline stack size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E93279A1-4238-49C7-8525-EE01999454D9">GetShaderIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier for a shader that can be used in a shader record.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C804CAF-7263-4E37-9C00-F85959CE651D">GetShaderStackSize</a>
</td>
<td align="left" width="63%">
Gets the amount of stack memory required to invoke a raytracing shader in HLSL.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0BB69DBB-F8A1-4C32-AE82-3A49E2E0E4B3">SetPipelineStackSize</a>
</td>
<td align="left" width="63%">
Set the current pipeline stack size.  

</td>
</tr>
</table> 

