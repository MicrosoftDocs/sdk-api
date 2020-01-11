---
UID: NN:d3d12sdklayers.ID3D12DebugCommandList1
title: ID3D12DebugCommandList1 (d3d12sdklayers.h)
description: This interface enables modification of additional command list debug layer settings.
old-location: direct3d12\id3d12debugcommandlist1.htm
tech.root: direct3d12
ms.assetid: 2DF22383-768C-4D23-9ED8-F0CFD6BA6EE7
ms.date: 12/05/2018
ms.keywords: ID3D12DebugCommandList1, ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,described, d3d12sdklayers/ID3D12DebugCommandList1, direct3d12.id3d12debugcommandlist1
f1_keywords:
- d3d12sdklayers/ID3D12DebugCommandList1
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
- ID3D12DebugCommandList1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DebugCommandList1 interface


## -description


This interface enables modification of additional command list debug layer settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DebugCommandList1</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12DebugCommandList1</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-assertresourcestate">AssertResourceState</a>
</td>
<td align="left" width="63%">
Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g. the resource was transitioned earlier in the same command list recording).  If the state is not yet known this method sets the known state for further validation later in the same command list recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter">GetDebugParameter</a>
</td>
<td align="left" width="63%">
Gets optional Command List Debug Layer settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter">SetDebugParameter</a>
</td>
<td align="left" width="63%">
Modifies optional Debug Layer settings of a command list.

</td>
</tr>
</table> 


## -remarks



This interface is currently in Preview mode.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

