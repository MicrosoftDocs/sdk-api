---
UID: NN:d3d12sdklayers.ID3D12DebugCommandList
title: ID3D12DebugCommandList (d3d12sdklayers.h)
description: Provides methods to monitor and debug a command list.helpviewer_keywords: ["ID3D12DebugCommandList","ID3D12DebugCommandList interface","ID3D12DebugCommandList interface","described","d3d12sdklayers/ID3D12DebugCommandList","direct3d12.id3d12debugcommandlist"]
old-location: direct3d12\id3d12debugcommandlist.htm
tech.root: direct3d12
ms.assetid: EDE527F0-4091-4B03-9030-6F693FE901BE
ms.date: 12/05/2018
ms.keywords: ID3D12DebugCommandList, ID3D12DebugCommandList interface, ID3D12DebugCommandList interface,described, d3d12sdklayers/ID3D12DebugCommandList, direct3d12.id3d12debugcommandlist
f1_keywords:
- d3d12sdklayers/ID3D12DebugCommandList
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DebugCommandList interface


## -description


Provides methods to monitor and debug a command list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugCommandList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12DebugCommandList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist-assertresourcestate">AssertResourceState</a>
</td>
<td align="left" width="63%">
Checks whether a resource, or subresource, is in a specified state, or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist-getfeaturemask">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Returns the debug feature flags that have been set on a command list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist-setfeaturemask">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Turns the debug features for a command list on or off.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

