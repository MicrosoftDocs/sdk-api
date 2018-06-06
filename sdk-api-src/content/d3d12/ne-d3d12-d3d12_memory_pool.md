---
UID: NE:d3d12.D3D12_MEMORY_POOL
title: D3D12_MEMORY_POOL
author: windows-sdk-content
description: Specifies the memory pool for the heap.
old-location: direct3d12\d3d12_memory_pool.htm
old-project: direct3d12
ms.assetid: EFA3FF00-F121-4ED8-AF83-1952C73AE06D
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_MEMORY_POOL, D3D12_MEMORY_POOL enumeration, D3D12_MEMORY_POOL_L0, D3D12_MEMORY_POOL_L1, D3D12_MEMORY_POOL_UNKNOWN, d3d12/D3D12_MEMORY_POOL, d3d12/D3D12_MEMORY_POOL_L0, d3d12/D3D12_MEMORY_POOL_L1, d3d12/D3D12_MEMORY_POOL_UNKNOWN, direct3d12.d3d12_memory_pool
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D12_MEMORY_POOL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_MEMORY_POOL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_MEMORY_POOL enumeration


## -description


Specifies the memory pool for the heap.


## -enum-fields




### -field D3D12_MEMORY_POOL_UNKNOWN


            The memory pool is unknown.
          


### -field D3D12_MEMORY_POOL_L0


            The memory pool is L0.
            L0 is the physical system memory pool.
            When the adapter is discrete/NUMA, this pool has greater bandwidth for the CPU and less bandwidth for the GPU.
            When the adapter is UMA, this pool is the only one which is valid.
          


### -field D3D12_MEMORY_POOL_L1


            The memory pool is L1.
            L1 is typically known as the physical video memory pool.
            L1 is only available when the adapter is discrete/NUMA, and has greater bandwidth for the GPU and cannot even be accessed by the CPU.
            When the adapter is UMA, this pool is not available.
          


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure.
      

When the adapter is UMA, D3D12_MEMORY_POOL_L0 and DXGI_MEMORY_SEGMENT_GROUP_LOCAL refer to the same memory.

When

 the adapter is not UMA:
D3D12_MEMORY_POOL_L0 and DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL refer to the same memory.
D3D12_MEMORY_POOL_L1 and DXGI_MEMORY_SEGMENT_GROUP_LOCAL refer to the same memory.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

