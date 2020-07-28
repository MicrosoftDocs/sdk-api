---
UID: NN:d3d12.ID3D12DescriptorHeap
title: ID3D12DescriptorHeap (d3d12.h)
description: A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.
helpviewer_keywords: ["ID3D12DescriptorHeap","ID3D12DescriptorHeap interface","ID3D12DescriptorHeap interface","described","d3d12/ID3D12DescriptorHeap","direct3d12.id3d12descriptorheap"]
old-location: direct3d12\id3d12descriptorheap.htm
tech.root: direct3d12
ms.assetid: B6FF011B-3FED-425B-B9D5-A823E6915FD5
ms.date: 12/05/2018
ms.keywords: ID3D12DescriptorHeap, ID3D12DescriptorHeap interface, ID3D12DescriptorHeap interface,described, d3d12/ID3D12DescriptorHeap, direct3d12.id3d12descriptorheap
f1_keywords:
- d3d12/ID3D12DescriptorHeap
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
- ID3D12DescriptorHeap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DescriptorHeap interface


## -description


A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor. Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DescriptorHeap</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12DescriptorHeap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12DescriptorHeap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart">GetCPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the CPU descriptor handle that represents the start of the heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the descriptor heap description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart">GetGPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the GPU descriptor handle that represents the start of the heap.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/creating-descriptor-heaps">Creating Descriptor Heaps</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>
 

 

