---
UID: NN:d3d12sdklayers.ID3D12DebugCommandList1
title: ID3D12DebugCommandList1
author: windows-sdk-content
description: This interface enables modification of additional command list debug layer settings.
old-location: direct3d12\id3d12debugcommandlist1.htm
tech.root: direct3d12
ms.assetid: 2DF22383-768C-4D23-9ED8-F0CFD6BA6EE7
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D12DebugCommandList1, ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,described, d3d12sdklayers/ID3D12DebugCommandList1, direct3d12.id3d12debugcommandlist1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandList1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList1 interface


## -description


This interface enables modification of additional command list debug layer settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugCommandList1</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12DebugCommandList1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DebugCommandList1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DB036A55-D677-4288-B165-5441BA457492">AssertResourceState</a>
</td>
<td align="left" width="63%">
Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g. the resource was transitioned earlier in the same command list recording).  If the state is not yet known this method sets the known state for further validation later in the same command list recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/936E9748-1D1A-46A9-B4FE-36C0C6627296">GetDebugParameter</a>
</td>
<td align="left" width="63%">
Gets optional Command List Debug Layer settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D93895A-BED7-4A86-893B-ACB5FA1B160F">SetDebugParameter</a>
</td>
<td align="left" width="63%">
Modifies optional Debug Layer settings of a command list.

</td>
</tr>
</table> 


## -remarks



This interface is currently in Preview mode.




## -see-also




<a href="https://msdn.microsoft.com/9BD5910A-8FF2-4540-BB8E-8EA5C10528CE">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

