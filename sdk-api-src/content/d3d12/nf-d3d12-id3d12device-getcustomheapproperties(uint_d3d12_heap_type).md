---
UID: NF:d3d12.ID3D12Device.GetCustomHeapProperties(UINT,D3D12_HEAP_TYPE)
title: ID3D12Device::GetCustomHeapProperties (d3d12.h)
description: Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties.
helpviewer_keywords: ["GetCustomHeapProperties","GetCustomHeapProperties method","GetCustomHeapProperties method","ID3D12Device interface","ID3D12Device interface","GetCustomHeapProperties method","ID3D12Device.GetCustomHeapProperties","ID3D12Device::GetCustomHeapProperties","d3d12/ID3D12Device::GetCustomHeapProperties","direct3d12.id3d12device_getcustomheapproperties"]
old-location: direct3d12\id3d12device_getcustomheapproperties.htm
tech.root: direct3d12
ms.assetid: FD1A7C77-24C3-49D5-8F20-01D5FF7FC895
ms.date: 12/05/2018
ms.keywords: GetCustomHeapProperties, GetCustomHeapProperties method, GetCustomHeapProperties method,ID3D12Device interface, ID3D12Device interface,GetCustomHeapProperties method, ID3D12Device.GetCustomHeapProperties, ID3D12Device::GetCustomHeapProperties, d3d12/ID3D12Device::GetCustomHeapProperties, direct3d12.id3d12device_getcustomheapproperties
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
 - ID3D12Device::GetCustomHeapProperties
 - d3d12/ID3D12Device::GetCustomHeapProperties
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
 - ID3D12Device.GetCustomHeapProperties
---

## -description

Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties.

## -parameters

### -param nodeMask [in]

Type: <b>UINT</b>

For single-GPU operation, set this to zero.
          If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter).
          Each bit in the mask corresponds to a single node.
          Only 1 bit must be set.
          See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -param heapType

Type: <b><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a></b>

A <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE</a>-typed value that specifies the heap to get properties for.
          D3D12_HEAP_TYPE_CUSTOM is not supported as a parameter value.

## -returns

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a></b>

Returns a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure that provides properties for the specified heap.
            The <b>Type</b> member of the returned D3D12_HEAP_PROPERTIES is always D3D12_HEAP_TYPE_CUSTOM.
          

When <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a>::UMA is FALSE, the returned D3D12_HEAP_PROPERTIES members convert as follows:
          

<table>
<tr>
<th>Heap Type</th>
<th>How the returned D3D12_HEAP_PROPERTIES members convert</th>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_UPLOAD</td>
<td><b>CPUPageProperty</b> = WRITE_COMBINE, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_DEFAULT</td>
<td><b>CPUPageProperty</b> = NOT_AVAILABLE, <b>MemoryPoolPreference</b> = L1.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_READBACK</td>
<td><b>CPUPageProperty</b> = WRITE_BACK, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
</table>
 

When D3D12_FEATURE_DATA_ARCHITECTURE::UMA is TRUE and D3D12_FEATURE_DATA_ARCHITECTURE::CacheCoherentUMA is FALSE, the returned D3D12_HEAP_PROPERTIES members convert as follows:
          

<table>
<tr>
<th>Heap Type</th>
<th>How the returned D3D12_HEAP_PROPERTIES members convert</th>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_UPLOAD</td>
<td><b>CPUPageProperty</b> = WRITE_COMBINE, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_DEFAULT</td>
<td><b>CPUPageProperty</b> = NOT_AVAILABLE, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_READBACK</td>
<td><b>CPUPageProperty</b> = WRITE_BACK, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
</table>
 

When D3D12_FEATURE_DATA_ARCHITECTURE::UMA is TRUE and D3D12_FEATURE_DATA_ARCHITECTURE::CacheCoherentUMA is TRUE, the returned D3D12_HEAP_PROPERTIES members convert as follows:
          

<table>
<tr>
<th>Heap Type</th>
<th>How the returned D3D12_HEAP_PROPERTIES members convert</th>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_UPLOAD</td>
<td><b>CPUPageProperty</b> = WRITE_BACK, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_DEFAULT</td>
<td><b>CPUPageProperty</b> = NOT_AVAILABLE, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
<tr>
<td>D3D12_HEAP_TYPE_READBACK</td>
<td><b>CPUPageProperty</b> = WRITE_BACK, <b>MemoryPoolPreference</b> = L0.
              </td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

