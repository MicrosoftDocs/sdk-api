---
UID: NN:d3d12sdklayers.ID3D12DebugCommandList
title: ID3D12DebugCommandList
author: windows-sdk-content
description: Provides methods to monitor and debug a command list.
old-location: direct3d12\id3d12debugcommandlist.htm
old-project: direct3d12
ms.assetid: EDE527F0-4091-4B03-9030-6F693FE901BE
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ID3D12DebugCommandList, ID3D12DebugCommandList interface, ID3D12DebugCommandList interface,described, d3d12sdklayers/ID3D12DebugCommandList, direct3d12.id3d12debugcommandlist
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugCommandList interface


## -description



          Provides methods to monitor and debug a command list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugCommandList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12DebugCommandList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DebugCommandList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9190760D-B624-4E3E-8C33-B5D888895499">AssertResourceState</a>
</td>
<td align="left" width="63%">

          Checks whether a resource, or subresource, is in a specified state, or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98FE1D2C-648B-4689-BE52-A53C969D9281">GetFeatureMask</a>
</td>
<td align="left" width="63%">

          Returns the debug feature flags that have been set on a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2273A6C-7401-44D6-A0E3-F3F2C5DBCB8B">SetFeatureMask</a>
</td>
<td align="left" width="63%">

          Turns the debug features for a command list on or off.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9BD5910A-8FF2-4540-BB8E-8EA5C10528CE">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

