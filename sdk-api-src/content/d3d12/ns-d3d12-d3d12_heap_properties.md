---
UID: NS:d3d12.D3D12_HEAP_PROPERTIES
title: D3D12_HEAP_PROPERTIES (d3d12.h)
description: Describes heap properties.
helpviewer_keywords: ["D3D12_HEAP_PROPERTIES","D3D12_HEAP_PROPERTIES structure","d3d12/D3D12_HEAP_PROPERTIES","direct3d12.d3d12_heap_properties"]
old-location: direct3d12\d3d12_heap_properties.htm
tech.root: direct3d12
ms.assetid: 0A197D3D-67F4-46BB-8578-15E05DF46067
ms.date: 12/05/2018
ms.keywords: D3D12_HEAP_PROPERTIES, D3D12_HEAP_PROPERTIES structure, d3d12/D3D12_HEAP_PROPERTIES, direct3d12.d3d12_heap_properties
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
req.typenames: D3D12_HEAP_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HEAP_PROPERTIES
 - d3d12/D3D12_HEAP_PROPERTIES
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
 - D3D12_HEAP_PROPERTIES
---

## -description

Describes heap properties.

## -struct-fields

### -field Type

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a>-typed value that specifies the type of heap.

### -field CPUPageProperty

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property">D3D12_CPU_PAGE_PROPERTY</a>-typed value that specifies the CPU-page properties for the heap.

### -field MemoryPoolPreference

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL</a>-typed value that specifies the memory pool for the heap.

### -field CreationNodeMask

For multi-adapter operation, this indicates the node where the resource should be created.

Exactly one bit of this UINT must be set. See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

Passing zero is equivalent to passing one, in order to simplify the usage of single-GPU adapters.

### -field VisibleNodeMask

For multi-adapter operation, this indicates the set of nodes where the resource is visible.

<i>VisibleNodeMask</i> must have the same bit set that is set in <i>CreationNodeMask</i>. <i>VisibleNodeMask</i> can *also* have additional bits set for cross-node resources, but doing so can potentially reduce performance for resource accesses, so you should do so only when needed.

Passing zero is equivalent to passing one, in order to simplify the usage of single-GPU adapters.

## -remarks

This structure is used by the following:

<ul>
<li>
<a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc">D3D12_HEAP_DESC</a> structure
          </li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getheapproperties">ID3D12Resource::GetHeapProperties</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties(uint_d3d12_heap_type)">ID3D12Device::GetCustomHeapProperties</a>
</li>
<li>
<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>
</li>
</ul>
Valid combinations of struct member values:

<ul>
<li>When <b>Type</b> is <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a>_CUSTOM,
            <b>CPUPageProperty</b> and <b>MemoryPoolPreference</b> must not be ..._UNKNOWN.
          </li>
<li>When <b>Type</b> is not D3D12_HEAP_TYPE_CUSTOM,
            <b>CPUPageProperty</b> and <b>MemoryPoolPreference</b> must be ..._UNKNOWN.
          </li>
<li>When using D3D12_HEAP_TYPE_CUSTOM and <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL</a>_L1, on NUMA adapters,
            <b>CPUPageProperty</b> must be <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property">D3D12_CPU_PAGE_PROPERTY</a>_NOT_AVAILABLE.
            To differentiate NUMA from UMA adapters, see
            <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>_ARCHITECTURE and
            <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a>.
          </li>
</ul>

## -see-also

<a href="/windows/win32/direct3d12/cd3dx12-heap-properties">CD3DX12_HEAP_PROPERTIES</a>

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core structures</a>

<a href="/windows/win32/direct3d12/descriptor-heaps">Descriptor heaps</a>
