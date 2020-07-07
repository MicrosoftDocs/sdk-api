---
UID: NN:d3d12.ID3D12Heap
title: ID3D12Heap (d3d12.h)
description: A heap is an abstraction of contiguous memory allocation, used to manage physical memory. This heap can be used with ID3D12Resource objects to support placed resources or reserved resources.
helpviewer_keywords: ["ID3D12Heap","ID3D12Heap interface","ID3D12Heap interface","described","d3d12/ID3D12Heap","direct3d12.id3d12heap"]
old-location: direct3d12\id3d12heap.htm
tech.root: direct3d12
ms.assetid: 3791C64F-76D7-4580-A444-F2CEA3EB10CE
ms.date: 12/05/2018
ms.keywords: ID3D12Heap, ID3D12Heap interface, ID3D12Heap interface,described, d3d12/ID3D12Heap, direct3d12.id3d12heap
f1_keywords:
- d3d12/ID3D12Heap
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
- ID3D12Heap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Heap interface


## -description


A heap  is an abstraction of contiguous memory allocation, used to manage physical memory. This heap can be used with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> objects to support placed resources or reserved resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Heap</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12Heap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Heap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/direct3d12/id3d12heap-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the heap description.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/memory-management">Memory Management in Direct3D 12</a>
 

 

