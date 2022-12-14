---
UID: NF:d3d12.ID3D12DescriptorHeap.GetGPUDescriptorHandleForHeapStart
title: ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart (d3d12.h)
description: Gets the GPU descriptor handle that represents the start of the heap.
helpviewer_keywords: ["GetGPUDescriptorHandleForHeapStart","GetGPUDescriptorHandleForHeapStart method","GetGPUDescriptorHandleForHeapStart method","ID3D12DescriptorHeap interface","ID3D12DescriptorHeap interface","GetGPUDescriptorHandleForHeapStart method","ID3D12DescriptorHeap.GetGPUDescriptorHandleForHeapStart","ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart","d3d12/ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart","direct3d12.id3d12descriptorheap_getgpudescriptorhandleforheapstart"]
old-location: direct3d12\id3d12descriptorheap_getgpudescriptorhandleforheapstart.htm
tech.root: direct3d12
ms.assetid: 63A031A1-EF53-4308-A8F9-179E21C7CE7B
ms.date: 12/05/2018
ms.keywords: GetGPUDescriptorHandleForHeapStart, GetGPUDescriptorHandleForHeapStart method, GetGPUDescriptorHandleForHeapStart method,ID3D12DescriptorHeap interface, ID3D12DescriptorHeap interface,GetGPUDescriptorHandleForHeapStart method, ID3D12DescriptorHeap.GetGPUDescriptorHandleForHeapStart, ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart, d3d12/ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart, direct3d12.id3d12descriptorheap_getgpudescriptorhandleforheapstart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart
 - d3d12/ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12DescriptorHeap.GetGPUDescriptorHandleForHeapStart
---

# ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart


## -description

Gets the GPU descriptor handle that represents the start of the heap.



## -returns

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

Returns the GPU descriptor handle that represents the start of the heap. If the descriptor heap is not shader-visible, a null handle is returned.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap">ID3D12DescriptorHeap</a>
