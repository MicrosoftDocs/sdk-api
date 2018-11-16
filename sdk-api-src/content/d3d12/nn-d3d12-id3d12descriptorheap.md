---
UID: NN:d3d12.ID3D12DescriptorHeap
title: ID3D12DescriptorHeap
author: windows-sdk-content
description: A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.
old-location: direct3d12\id3d12descriptorheap.htm
tech.root: direct3d12
ms.assetid: B6FF011B-3FED-425B-B9D5-A823E6915FD5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12DescriptorHeap, ID3D12DescriptorHeap interface, ID3D12DescriptorHeap interface,described, d3d12/ID3D12DescriptorHeap, direct3d12.id3d12descriptorheap
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12DescriptorHeap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DescriptorHeap interface


## -description


A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor. Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12DescriptorHeap</b> interface inherits from <a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>. <b>ID3D12DescriptorHeap</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn899174(v=VS.85).aspx">GetCPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the CPU descriptor handle that represents the start of the heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn788649(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the descriptor heap description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn899175(v=VS.85).aspx">GetGPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the GPU descriptor handle that represents the start of the heap.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770457(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859359(v=VS.85).aspx">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

