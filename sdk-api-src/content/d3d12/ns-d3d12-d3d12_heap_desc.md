---
UID: NS:d3d12.D3D12_HEAP_DESC
title: D3D12_HEAP_DESC (d3d12.h)
description: Describes a heap.
helpviewer_keywords: ["D3D12_HEAP_DESC","D3D12_HEAP_DESC structure","d3d12/D3D12_HEAP_DESC","direct3d12.d3d12_heap_desc"]
old-location: direct3d12\d3d12_heap_desc.htm
tech.root: direct3d12
ms.assetid: 3A473476-F37E-4F01-B121-87E998EE9411
ms.date: 12/05/2018
ms.keywords: D3D12_HEAP_DESC, D3D12_HEAP_DESC structure, d3d12/D3D12_HEAP_DESC, direct3d12.d3d12_heap_desc
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
req.typenames: D3D12_HEAP_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HEAP_DESC
 - d3d12/D3D12_HEAP_DESC
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
 - D3D12_HEAP_DESC
---

# D3D12_HEAP_DESC structure


## -description

Describes a heap.

## -struct-fields

### -field SizeInBytes

The size, in bytes, of the heap.
            To avoid wasting memory, applications should pass <i>SizeInBytes</i> values which are multiples of the effective <i>Alignment</i>;
            but non-aligned <i>SizeInBytes</i> is also supported, for convenience.
            To find out how large a heap must be to support textures with undefined layouts and adapter-specific sizes, call <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo(uint_uint_constd3d12_resource_desc)">ID3D12Device::GetResourceAllocationInfo</a>.

### -field Properties

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure that describes the heap properties.

### -field Alignment

The alignment value for the heap.  Valid values:
            

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0
                </td>
<td>An alias for 64KB.
                </td>
</tr>
<tr>
<td>D3D12_DEFAULT_RESOURCE_PLACEMENT_ALIGNMENT
                </td>
<td>#defined as 64KB.
                </td>
</tr>
<tr>
<td>D3D12_DEFAULT_MSAA_RESOURCE_PLACEMENT_ALIGNMENT
                </td>
<td>#defined as 4MB.
                  An application must decide whether the heap will contain multi-sample anti-aliasing (MSAA), in which case, the application must choose D3D12_DEFAULT_MSAA_RESOURCE_PLACEMENT_ALIGNMENT.
                </td>
</tr>
</table>

### -field Flags

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a>-typed values that are combined by using a bitwise-OR operation.
            The resulting value identifies heap options.
            When creating heaps to support adapters with resource heap tier 1, an application must choose some flags.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">CreateHeap</a> method, and returned by the <a href="/windows/desktop/direct3d12/id3d12heap-getdesc">GetDesc</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-heap-desc">CD3DX12_HEAP_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>