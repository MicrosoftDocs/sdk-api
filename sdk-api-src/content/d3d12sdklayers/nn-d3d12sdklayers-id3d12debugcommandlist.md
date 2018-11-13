---
UID: NN:d3d12sdklayers.ID3D12DebugCommandList
title: ID3D12DebugCommandList
author: windows-sdk-content
description: Provides methods to monitor and debug a command list.
old-location: direct3d12\id3d12debugcommandlist.htm
tech.root: direct3d12
ms.assetid: EDE527F0-4091-4B03-9030-6F693FE901BE
ms.author: windowssdkdev
ms.date: 11/12/2018
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
 - ID3D12DebugCommandList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList interface


## -description


Provides methods to monitor and debug a command list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugCommandList</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D12DebugCommandList</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn950155(v=VS.85).aspx">AssertResourceState</a>
</td>
<td align="left" width="63%">
Checks whether a resource, or subresource, is in a specified state, or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950156(v=VS.85).aspx">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Returns the debug feature flags that have been set on a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn950157(v=VS.85).aspx">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Turns the debug features for a command list on or off.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950150(v=VS.85).aspx">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

