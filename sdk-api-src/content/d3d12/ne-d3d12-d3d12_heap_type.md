---
UID: NE:d3d12.D3D12_HEAP_TYPE
title: D3D12_HEAP_TYPE (d3d12.h)
description: Specifies the type of heap. When resident, heaps reside in a particular physical memory pool with certain CPU cache properties.
helpviewer_keywords: ["D3D12_HEAP_TYPE","D3D12_HEAP_TYPE enumeration","D3D12_HEAP_TYPE_CUSTOM","D3D12_HEAP_TYPE_DEFAULT","D3D12_HEAP_TYPE_READBACK","D3D12_HEAP_TYPE_UPLOAD","d3d12/D3D12_HEAP_TYPE","d3d12/D3D12_HEAP_TYPE_CUSTOM","d3d12/D3D12_HEAP_TYPE_DEFAULT","d3d12/D3D12_HEAP_TYPE_READBACK","d3d12/D3D12_HEAP_TYPE_UPLOAD","direct3d12.d3d12_heap_type"]
old-location: direct3d12\d3d12_heap_type.htm
tech.root: direct3d12
ms.assetid: 5B1EA8A6-BD59-4B92-B6C4-A5C26D0B16D4
ms.date: 12/05/2018
ms.keywords: D3D12_HEAP_TYPE, D3D12_HEAP_TYPE enumeration, D3D12_HEAP_TYPE_CUSTOM, D3D12_HEAP_TYPE_DEFAULT, D3D12_HEAP_TYPE_READBACK, D3D12_HEAP_TYPE_UPLOAD, d3d12/D3D12_HEAP_TYPE, d3d12/D3D12_HEAP_TYPE_CUSTOM, d3d12/D3D12_HEAP_TYPE_DEFAULT, d3d12/D3D12_HEAP_TYPE_READBACK, d3d12/D3D12_HEAP_TYPE_UPLOAD, direct3d12.d3d12_heap_type
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
req.typenames: D3D12_HEAP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HEAP_TYPE
 - d3d12/D3D12_HEAP_TYPE
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
 - D3D12_HEAP_TYPE
---

# D3D12_HEAP_TYPE enumeration


## -description

Specifies the type of heap.
          When resident, heaps reside in a particular physical memory pool with certain CPU cache properties.

## -enum-fields

### -field D3D12_HEAP_TYPE_DEFAULT:1

Specifies the default heap.
            This heap type experiences the most bandwidth for the GPU, but cannot provide CPU access.
            The GPU can read and write to the memory from this pool, and resource transition barriers may be changed.
            The majority of heaps and resources are expected to be located here, and are typically populated through resources in upload heaps.

### -field D3D12_HEAP_TYPE_UPLOAD:2

Specifies a heap used for uploading.
              This heap type has CPU access optimized for uploading to the GPU, but does not experience the maximum amount of bandwidth for the GPU.
              This heap type is best for CPU-write-once, GPU-read-once data; but GPU-read-once is stricter than necessary.
              GPU-read-once-or-from-cache is an acceptable use-case for the data; but such usages are hard to judge due to differing GPU cache designs and sizes.
              If in doubt, stick to the GPU-read-once definition or profile the difference on many GPUs between copying the data to a _DEFAULT heap vs. reading the data from an _UPLOAD heap.
            

Resources in this heap must be created with <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE</a>_GENERIC_READ and cannot be changed away from this.
              The CPU address for such heaps is commonly not efficient for CPU reads.
            

The following are typical usages for _UPLOAD heaps:
            

<ul>
<li>Initializing resources in a _DEFAULT heap with data from the CPU.
              </li>
<li>Uploading dynamic data in a constant buffer that is read, repeatedly, by each vertex or pixel.
              </li>
</ul>
The following are likely not good usages for _UPLOAD heaps:
            

<ul>
<li>Re-initializing the contents of a resource every frame.
              </li>
<li>Uploading constant data which is only used every other Draw call, where each Draw uses a non-trivial amount of other data.
              </li>
</ul>

### -field D3D12_HEAP_TYPE_READBACK:3

Specifies a heap used for reading back.
              This heap type has CPU access optimized for reading data back from the GPU, but does not experience the maximum amount of bandwidth for the GPU.
              This heap type is best for GPU-write-once, CPU-readable data.
              The CPU cache behavior is write-back, which is conducive for multiple sub-cache-line CPU reads.
            

Resources in this heap must be created with <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE</a>_COPY_DEST, and cannot be changed away from this.

### -field D3D12_HEAP_TYPE_CUSTOM:4

Specifies a custom heap.
            The application may specify the memory pool and CPU cache properties directly, which can be useful for UMA optimizations, multi-engine, multi-adapter, or other special cases.
            To do so, the application is expected to understand the adapter architecture to make the right choice.
            For more details, see 
            <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>_ARCHITECTURE, 
            <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a>, and 
            <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties">GetCustomHeapProperties</a>.

## -remarks

This enum is used by the following API items:
        

<ul>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc">D3D12_HEAP_DESC</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties">GetCustomHeapProperties</a>
</li>
</ul>
The heap types fall into two categories: abstracted heap types, and custom heap types.
        

The following are abstracted heap types:
        

<ul>
<li>D3D12_HEAP_TYPE_DEFAULT</li>
<li>D3D12_HEAP_TYPE_UPLOAD</li>
<li>D3D12_HEAP_TYPE_READBACK</li>
</ul>
The following is a custom heap type:
        

<ul>
<li>D3D12_HEAP_TYPE_CUSTOM</li>
</ul>
The abstracted heap types (_DEFAULT, _UPLOAD, and _READBACK) are useful to simplify writing adapter-neutral applications, because such applications don't need to be aware of the adapter memory architecture.
          To use an abstracted heap type to simplify writing adapter-neutral applications, the application essentially treats the adapter as if it were a discrete or NUMA adapter.
          But, using the heap types enables efficient translation for UMA adapters.
          Adapter architecture neutral applications should assume there are two memory pools available, where the pool with the most GPU bandwidth cannot provide CPU access.
          The pool with the least GPU bandwidth can have CPU access; but must be either optimized for upload to GPU or readback from GPU.
        



Note that textures (unlike buffers) can't be heap type UPLOAD or READBACK.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>
