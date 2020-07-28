---
UID: NN:d3d12.ID3D12Fence
title: ID3D12Fence (d3d12.h)
description: Represents a fence, an object used for synchronization of the CPU and one or more GPUs.
helpviewer_keywords: ["ID3D12Fence","ID3D12Fence interface","ID3D12Fence interface","described","d3d12/ID3D12Fence","direct3d12.id3d12fence"]
old-location: direct3d12\id3d12fence.htm
tech.root: direct3d12
ms.assetid: 2B388352-EF43-4D1E-851C-A670B4681F0F
ms.date: 12/05/2018
ms.keywords: ID3D12Fence, ID3D12Fence interface, ID3D12Fence interface,described, d3d12/ID3D12Fence, direct3d12.id3d12fence
f1_keywords:
- d3d12/ID3D12Fence
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
- ID3D12Fence
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Fence interface


## -description


Represents a fence, an object used for synchronization of the CPU and one or more GPUs. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Fence</b> interface inherits from <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12Fence</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Fence</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue">GetCompletedValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the fence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion">SetEventOnCompletion</a>
</td>
<td align="left" width="63%">
Specifies an event that should be fired when the fence reaches a certain value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal">Signal</a>
</td>
<td align="left" width="63%">
Sets the fence to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/win32/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/win32/direct3d12/fence-based-resource-management">Fence Based Resource Management</a>



<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>
 

 

