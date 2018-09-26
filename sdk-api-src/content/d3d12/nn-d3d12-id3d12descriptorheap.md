---
UID: NN:d3d12.ID3D12DescriptorHeap
title: ID3D12DescriptorHeap
author: windows-sdk-content
description: A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.
old-location: direct3d12\id3d12descriptorheap.htm
tech.root: direct3d12
ms.assetid: B6FF011B-3FED-425B-B9D5-A823E6915FD5
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID3D12DescriptorHeap, ID3D12DescriptorHeap interface, ID3D12DescriptorHeap interface,described, d3d12/ID3D12DescriptorHeap, direct3d12.id3d12descriptorheap
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
<a href="https://msdn.microsoft.com/80C41537-1579-4166-A7F9-FB2478ECDE77">GetCPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the CPU descriptor handle that represents the start of the heap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDDDA9AB-841A-41A4-806C-82A596AFDB61">GetDesc</a>
</td>
<td align="left" width="63%">
Gets the descriptor heap description.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63A031A1-EF53-4308-A8F9-179E21C7CE7B">GetGPUDescriptorHandleForHeapStart</a>
</td>
<td align="left" width="63%">
Gets the GPU descriptor handle that represents the start of the heap.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/58677023-692C-4BA4-90B7-D568F3DD3F73">Creating Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>



<a href="https://msdn.microsoft.com/89DC88B4-9DFD-413D-8EB9-91087CC90D18">ID3D12Pageable</a>
 

 

