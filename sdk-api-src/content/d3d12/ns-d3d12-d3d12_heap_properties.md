---
UID: NS:d3d12.D3D12_HEAP_PROPERTIES
title: D3D12_HEAP_PROPERTIES
author: windows-sdk-content
description: Describes heap properties.
old-location: direct3d12\d3d12_heap_properties.htm
tech.root: direct3d12
ms.assetid: 0A197D3D-67F4-46BB-8578-15E05DF46067
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_HEAP_PROPERTIES, D3D12_HEAP_PROPERTIES structure, d3d12/D3D12_HEAP_PROPERTIES, direct3d12.d3d12_heap_properties
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_HEAP_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D3D12_HEAP_PROPERTIES
req.redist: 
---

# D3D12_HEAP_PROPERTIES structure


## -description


Describes heap properties.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/5B1EA8A6-BD59-4B92-B6C4-A5C26D0B16D4">D3D12_HEAP_TYPE</a>-typed value that specifies the type of heap.
          


### -field CPUPageProperty

A <a href="https://msdn.microsoft.com/92C1DBB9-213C-4623-B6AA-B790E081F123">D3D12_CPU_PAGE_PROPERTY</a>-typed value that specifies the CPU-page properties for the heap.
          


### -field MemoryPoolPreference

A <a href="https://msdn.microsoft.com/EFA3FF00-F121-4ED8-AF83-1952C73AE06D">D3D12_MEMORY_POOL</a>-typed value that specifies the memory pool for the heap.
          


### -field CreationNodeMask

For multi-adapter operation, this indicates the node where the resource should be created.
              Exactly one bit of this UINT must be set.
              See <a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>.
            

Passing zero is equivalent to passing one, in order to simplify the usage of single-GPU adapters.
            


### -field VisibleNodeMask

For multi-adapter operation, this indicates the set of nodes where the resource is visible.
              <i>VisibleNodeMask</i> must have the same bits set as <i>CreationNodeMask</i> has.
              See <a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>.
            

Passing zero is equivalent to passing one, in order to simplify the usage of single-GPU adapters.
            


## -remarks



This structure is used by the following:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/3A473476-F37E-4F01-B121-87E998EE9411">D3D12_HEAP_DESC</a> structure
          </li>
<li>
<a href="https://msdn.microsoft.com/7F76986D-02F1-4E5A-B9A4-CFB021B72026">ID3D12Resource::GetHeapProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FD1A7C77-24C3-49D5-8F20-01D5FF7FC895">ID3D12Device::GetCustomHeapProperties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>
</li>
</ul>
Valid combinations of struct member values:
        

<ul>
<li>When <b>Type</b> is <a href="https://msdn.microsoft.com/5B1EA8A6-BD59-4B92-B6C4-A5C26D0B16D4">D3D12_HEAP_TYPE</a>_CUSTOM,
            <b>CPUPageProperty</b> and <b>MemoryPoolPreference</b> must not be ..._UNKNOWN.
          </li>
<li>When <b>Type</b> is not D3D12_HEAP_TYPE_CUSTOM,
            <b>CPUPageProperty</b> and <b>MemoryPoolPreference</b> must be ..._UNKNOWN.
          </li>
<li>When using D3D12_HEAP_TYPE_CUSTOM and <a href="https://msdn.microsoft.com/EFA3FF00-F121-4ED8-AF83-1952C73AE06D">D3D12_MEMORY_POOL</a>_L1, on NUMA adapters,
            <b>CPUPageProperty</b> must be <a href="https://msdn.microsoft.com/92C1DBB9-213C-4623-B6AA-B790E081F123">D3D12_CPU_PAGE_PROPERTY</a>_NOT_AVAILABLE.
            To differentiate NUMA from UMA adapters, see
            <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>_ARCHITECTURE and
            <a href="https://msdn.microsoft.com/FA16A260-3CC9-4F32-A97B-8A561A01C138">D3D12_FEATURE_DATA_ARCHITECTURE</a>.
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/AC759F25-D643-412D-AA83-3A2C040BE64B">CD3DX12_HEAP_PROPERTIES</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

