---
UID: NE:d3d12.D3D12_MEMORY_POOL
title: D3D12_MEMORY_POOL (d3d12.h)
description: Specifies the memory pool for the heap.
helpviewer_keywords: ["D3D12_MEMORY_POOL","D3D12_MEMORY_POOL enumeration","D3D12_MEMORY_POOL_L0","D3D12_MEMORY_POOL_L1","D3D12_MEMORY_POOL_UNKNOWN","d3d12/D3D12_MEMORY_POOL","d3d12/D3D12_MEMORY_POOL_L0","d3d12/D3D12_MEMORY_POOL_L1","d3d12/D3D12_MEMORY_POOL_UNKNOWN","direct3d12.d3d12_memory_pool"]
old-location: direct3d12\d3d12_memory_pool.htm
tech.root: direct3d12
ms.assetid: EFA3FF00-F121-4ED8-AF83-1952C73AE06D
ms.date: 12/05/2018
ms.keywords: D3D12_MEMORY_POOL, D3D12_MEMORY_POOL enumeration, D3D12_MEMORY_POOL_L0, D3D12_MEMORY_POOL_L1, D3D12_MEMORY_POOL_UNKNOWN, d3d12/D3D12_MEMORY_POOL, d3d12/D3D12_MEMORY_POOL_L0, d3d12/D3D12_MEMORY_POOL_L1, d3d12/D3D12_MEMORY_POOL_UNKNOWN, direct3d12.d3d12_memory_pool
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
req.typenames: D3D12_MEMORY_POOL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MEMORY_POOL
 - d3d12/D3D12_MEMORY_POOL
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
 - D3D12_MEMORY_POOL
---

# D3D12_MEMORY_POOL enumeration


## -description

Specifies the memory pool for the heap.

## -enum-fields

### -field D3D12_MEMORY_POOL_UNKNOWN:0

The memory pool is unknown.

### -field D3D12_MEMORY_POOL_L0:1

The memory pool is L0.
            L0 is the physical system memory pool.
            When the adapter is discrete/NUMA, this pool has greater bandwidth for the CPU and less bandwidth for the GPU.
            When the adapter is UMA, this pool is the only one which is valid.

### -field D3D12_MEMORY_POOL_L1:2

The memory pool is L1.
            L1 is typically known as the physical video memory pool.
            L1 is only available when the adapter is discrete/NUMA, and has greater bandwidth for the GPU and cannot even be accessed by the CPU.
            When the adapter is UMA, this pool is not available.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure.
      

When the adapter is UMA, D3D12_MEMORY_POOL_L0 and DXGI_MEMORY_SEGMENT_GROUP_LOCAL refer to the same memory.

When

 the adapter is not UMA:
D3D12_MEMORY_POOL_L0 and DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL refer to the same memory.
D3D12_MEMORY_POOL_L1 and DXGI_MEMORY_SEGMENT_GROUP_LOCAL refer to the same memory.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>
