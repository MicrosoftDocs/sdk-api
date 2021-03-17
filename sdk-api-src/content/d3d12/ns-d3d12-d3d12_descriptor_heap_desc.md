---
UID: NS:d3d12.D3D12_DESCRIPTOR_HEAP_DESC
title: D3D12_DESCRIPTOR_HEAP_DESC (d3d12.h)
description: Describes the descriptor heap.
helpviewer_keywords: ["D3D12_DESCRIPTOR_HEAP_DESC","D3D12_DESCRIPTOR_HEAP_DESC structure","d3d12/D3D12_DESCRIPTOR_HEAP_DESC","direct3d12.d3d12_descriptor_heap_desc"]
old-location: direct3d12\d3d12_descriptor_heap_desc.htm
tech.root: direct3d12
ms.assetid: 060ED49E-12B2-4DAE-A9DC-5BAB96B8E8ED
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_HEAP_DESC, D3D12_DESCRIPTOR_HEAP_DESC structure, d3d12/D3D12_DESCRIPTOR_HEAP_DESC, direct3d12.d3d12_descriptor_heap_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_DESCRIPTOR_HEAP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_HEAP_DESC
 - d3d12/D3D12_DESCRIPTOR_HEAP_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DESCRIPTOR_HEAP_DESC
---

# D3D12_DESCRIPTOR_HEAP_DESC structure


## -description

Describes the descriptor heap.

## -struct-fields

### -field Type

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the types of descriptors in the heap.

### -field NumDescriptors

The number of descriptors in the heap.

### -field Flags

A combination of <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags">D3D12_DESCRIPTOR_HEAP_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for the heap.

### -field NodeMask

For single-adapter operation, set this to zero.
            If there are multiple adapter nodes, set a bit to identify the node (one of the device's physical adapters) to which the descriptor heap applies.
            Each bit in the mask corresponds to a single node.
            Only one bit must be set.
            See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

## -remarks

This structure is used by the following:
        

<ul>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getdesc">ID3D12DescriptorHeap::GetDesc</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap">ID3D12Device::CreateDescriptorHeap</a>
</li>
</ul>

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/win32/direct3d12/creating-descriptor-heaps">Creating Descriptor Heaps</a>



<a href="/windows/win32/direct3d12/descriptor-heaps">Descriptor Heaps</a>

