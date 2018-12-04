---
UID: NS:d3d12.D3D12_HEAP_DESC
title: D3D12_HEAP_DESC
author: windows-sdk-content
description: Describes a heap.
old-location: direct3d12\d3d12_heap_desc.htm
tech.root: direct3d12
ms.assetid: 3A473476-F37E-4F01-B121-87E998EE9411
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_HEAP_DESC, D3D12_HEAP_DESC structure, d3d12/D3D12_HEAP_DESC, direct3d12.d3d12_heap_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12_HEAP_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_HEAP_DESC
req.redist: 
---

# D3D12_HEAP_DESC structure


## -description


Describes a heap.


## -struct-fields




### -field SizeInBytes

The size, in bytes, of the heap.
            To avoid wasting memory, applications should pass <i>SizeInBytes</i> values which are multiples of the effective <i>Alignment</i>;
            but non-aligned <i>SizeInBytes</i> is also supported, for convenience.
            To find out how large a heap must be to support textures with undefined layouts and adapter-specific sizes, call <a href="https://msdn.microsoft.com/43467E09-835B-4DB9-B0A4-F75868DE4609">ID3D12Device::GetResourceAllocationInfo</a>.
          


### -field Properties

A <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure that describes the heap properties.
          


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

A combination of <a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a>-typed values that are combined by using a bitwise-OR operation.
            The resulting value identifies heap options.
            When creating heaps to support adapters with resource heap tier 1, an application must choose some flags.
          


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">CreateHeap</a> method, and returned by the <a href="https://msdn.microsoft.com/45237F32-FBDE-49FF-926F-80B914B36AE5">GetDesc</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6">CD3DX12_HEAP_DESC</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

