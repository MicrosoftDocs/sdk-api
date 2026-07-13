---
UID: NS:d3d12.D3D12_FEATURE_DATA_ARCHITECTURE1
title: D3D12_FEATURE_DATA_ARCHITECTURE1 (d3d12.h)
description: Provides detail about each adapter's architectural details, so that your application can better optimize for certain adapter properties.
helpviewer_keywords: ["D3D12_FEATURE_DATA_ARCHITECTURE1","D3D12_FEATURE_DATA_ARCHITECTURE1 structure","d3d12/D3D12_FEATURE_DATA_ARCHITECTURE1","direct3d12.d3d12_feature_data_architecture1"]
old-location: direct3d12\d3d12_feature_data_architecture1.htm
tech.root: direct3d12
ms.assetid: 635091FE-2756-4648-958E-0C13BDD50851
ms.date: 08/10/2022
ms.keywords: D3D12_FEATURE_DATA_ARCHITECTURE1, D3D12_FEATURE_DATA_ARCHITECTURE1 structure, d3d12/D3D12_FEATURE_DATA_ARCHITECTURE1, direct3d12.d3d12_feature_data_architecture1
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
req.typenames: D3D12_FEATURE_DATA_ARCHITECTURE1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_ARCHITECTURE1
 - d3d12/D3D12_FEATURE_DATA_ARCHITECTURE1
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
 - D3D12_FEATURE_DATA_ARCHITECTURE1
---

# D3D12_FEATURE_DATA_ARCHITECTURE1 structure


## -description

Provides detail about each adapter's architectural details, so that your application can better optimize for certain adapter properties.
<div class="alert"><b>Note</b>  This structure, introduced in Windows 10, version 1703 (Creators' Update), supersedes the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a> structure. If your application targets  Windows 10, version 1703 (Creators' Update) or higher, then use <b>D3D12_FEATURE_DATA_ARCHITECTURE1</b> (and <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE_ARCHITECTURE1</a>).</div><div> </div>

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device is relevant.
            See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.
            <b>NodeIndex</b> is filled out by the application before calling <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a>, as the application can retrieve details about the architecture of each adapter.

### -field TileBasedRenderer

Specifies whether the hardware and driver support a tile-based renderer.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support a tile-based renderer.

### -field UMA

Specifies whether the hardware and driver support UMA.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support UMA.

### -field CacheCoherentUMA

Specifies whether the hardware and driver support cache-coherent UMA.
            The runtime sets this member to <b>TRUE</b> if the hardware and driver support cache-coherent UMA.

### -field IsolatedMMU

<a href="/visualstudio/code-quality/annotating-structs-and-classes">SAL</a>: <code>_Out_</code>

Specifies whether the hardware and driver support isolated Memory Management Unit (MMU).
            The runtime sets this member to <b>TRUE</b> if the GPU honors CPU page table properties like <b>MEM_WRITE_WATCH</b> (for more information, see <a href="/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>) and <b>PAGE_READONLY</b> (for more information, see <a href="/windows/win32/Memory/memory-protection-constants">Memory Protection Constants</a>).

If <b>TRUE</b>, the application must take care to no use memory with these page table properties with the GPU, as the GPU might trigger these page table properties in unexpected ways. For example, GPU write operations might be coarser than the application expects, particularly writes from within shaders. Certain write-watch pages might appear dirty, even when it isn't obvious how GPU writes may have affected them. GPU operations associated with upload and readback heap usage scenarios work well with write-watch pages, but might occasionally generate false positives that can be safely ignored.

## -remarks

<h3><a id="How_to_use_UMA_and_CacheCoherentUMA"></a><a id="how_to_use_uma_and_cachecoherentuma"></a><a id="HOW_TO_USE_UMA_AND_CACHECOHERENTUMA"></a>How to use UMA and CacheCoherentUMA</h3>
D3D12 apps should be concerned about managing memory residency and providing the optimal heap properties.
            D3D12 apps can stay simplified and run reasonably well across many GPU architectures by only managing the residency for resources in <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a>_DEFAULT heaps.
            Those apps only need to call <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">IDXGIAdapter3::QueryVideoMemoryInfo</a> for DXGI_MEMORY_SEGMENT_GROUP_LOCAL, 
            and they must be tolerant that D3D12_HEAP_TYPE_UPLOAD and D3D12_HEAP_TYPE_READBACK come from that same memory segment group.
          

However, such a simple design is too constraining for applications that push the limits.
            So, D3D12_FEATURE_DATA_ARCHITECTURE helps applications better optimize for the underlying adapter properties.
          

Some applications may want to better optimize for discrete adapters, and take on the additional complexity of managing both system memory and video memory budgets.
            If the size of upload heaps rivals the size of default textures, a near doubling of memory utilization is available.
            When supporting such optimizations, an application can either detect two residency budgets or recognize <b>UMA</b> is <b>false</b>.
          

Some applications may want to better optimize for integrated/ UMA adapters, especially those that are interested in extending battery life on mobile device.
            Simple D3D12 applications are forced into copying data between heaps with different attributions, when it isn't always necessary on UMA.
            However, the UMA property, by itself, encompasses a reasonably vague grey area of GPU designs.
            Do not assume UMA means all GPU-accessible memory can be freely made CPU-accessible, because it doesn't.
            There's a property that more closely aligns to that type of thinking: <b>CacheCoherentUMA</b>.
          

When <b>CacheCoherentUMA</b> is <b>false</b>, a single residency budget is available but the UMA design commonly benefits from the three heap attributions.
            Opportunities do exist to remove resource copying through wise usage of upload and readback resources and heaps, that provide CPU-access to the memory.
            Such opportunities are not clear-cut, though.
            So, applications should be cautious; and experimentation across a variety of "UMA" systems is advisable, as resorting to enabling or precluding certain device IDs may be warranted.
            An understanding of the GPU memory architecture and how heap types translate to cache properties is recommended.
            The feasibility of success is likely dependent on how often each processor either reads or writes the data, the size and locality of data accesses, etc.
            For advanced developers: when <b>UMA</b> is true and <b>CacheCoherentUMA</b> is <b>false</b>, the most unique characteristic for these adapters is that upload heaps are still write-combined.
            However, some UMA adapters benefit from both the no-CPU-access and write-combine properties of default and upload heaps.
            See <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties(uint_d3d12_heap_type)">GetCustomHeapProperties</a> for more details.
          

When <b>CacheCoherentUMA</b> is true, applications can more strongly entertain abandoning the attribution of heaps and using the custom heap equivalent of upload heaps everywhere.
            Zero-copy UMA optimizations such those offered by 
            <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a> are more generally encouraged as more scenarios will just benefit from shared usage.
            The memory model is very conducive to more scenarios and wider adoption.
            Some corner cases may still exist where benefits are not easily obtained, but they should be much rarer and less detrimental than other options.
            For advanced developers: <b>CacheCoherentUMA</b> means that a significant amount of the caches in the memory hierarchy are also unified or integrated between the CPU and GPU.
            The most unique observable characteristic is that upload heaps are actually write-back on <b>CacheCoherentUMA</b>.
            For these architecture, the usage of write-combine on upload heaps is commonly a detriment.
          

The low-level details should be ignored by a vast majority of single-adapter applications.
            As usual, single-adapter applications can simplify the landscape and ensure that the CPU writes to upload heaps use patterns that are write-combine-friendly.
            The lower-level details help reinforce the concepts for multi-adapter applications.
            Multi-adapter applications likely need to understand adapter architecture properties well enough to choose the optimal custom heap properties to efficiently move data between adapters.

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
