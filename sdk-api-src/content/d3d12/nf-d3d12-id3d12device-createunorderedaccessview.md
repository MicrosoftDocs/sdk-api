---
UID: NF:d3d12.ID3D12Device.CreateUnorderedAccessView
title: ID3D12Device::CreateUnorderedAccessView (d3d12.h)
description: Creates a view for unordered accessing.
helpviewer_keywords: ["CreateUnorderedAccessView","CreateUnorderedAccessView method","CreateUnorderedAccessView method","ID3D12Device interface","ID3D12Device interface","CreateUnorderedAccessView method","ID3D12Device.CreateUnorderedAccessView","ID3D12Device::CreateUnorderedAccessView","d3d12/ID3D12Device::CreateUnorderedAccessView","direct3d12.id3d12device_createunorderedaccessview"]
old-location: direct3d12\id3d12device_createunorderedaccessview.htm
tech.root: direct3d12
ms.assetid: E834E469-2958-44A9-978F-F42D6BB6B1DC
ms.date: 12/05/2018
ms.keywords: CreateUnorderedAccessView, CreateUnorderedAccessView method, CreateUnorderedAccessView method,ID3D12Device interface, ID3D12Device interface,CreateUnorderedAccessView method, ID3D12Device.CreateUnorderedAccessView, ID3D12Device::CreateUnorderedAccessView, d3d12/ID3D12Device::CreateUnorderedAccessView, direct3d12.id3d12device_createunorderedaccessview
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
 - ID3D12Device::CreateUnorderedAccessView
 - d3d12/ID3D12Device::CreateUnorderedAccessView
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
 - ID3D12Device.CreateUnorderedAccessView
---

## -description

Creates a view for unordered accessing.

## -parameters

### -param pResource

Type: [in, optional] <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the unordered access.
          
At least one of <i>pResource</i> or <i>pDesc</i> must be provided.

A null <i>pResource</i> is used to initialize a null descriptor, which guarantees Direct3D 11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.

### -param pCounterResource

Type: [in, optional] <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

The <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> for the counter (if any) associated with the UAV.

If <i>pCounterResource</i> is not specified, then the <b>CounterOffsetInBytes</b> member of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav">D3D12_BUFFER_UAV</a> structure must be 0.

If <i>pCounterResource</i> is specified, then there is a counter associated with the UAV, and the runtime performs validation of the following requirements:

<ul>
<li>The <b>StructureByteStride</b> member of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav">D3D12_BUFFER_UAV</a> structure must be greater than 0.
              </li>
<li>The format must be DXGI_FORMAT_UNKNOWN.
              </li>
<li>The D3D12_BUFFER_UAV_FLAG_RAW flag (a <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags">D3D12_BUFFER_UAV_FLAGS</a> enumeration constant) must not be set.
              </li>
<li>Both of the resources (<i>pResource</i> and <i>pCounterResource</i>) must be buffers.
              </li>
<li>The <b>CounterOffsetInBytes</b> member of the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav">D3D12_BUFFER_UAV</a> structure must be a multiple of **D3D12_UAV_COUNTER_PLACEMENT_ALIGNMENT** (4096), and must be within the range of the counter resource.
              </li>
<li><i>pResource</i> cannot be NULL
              </li>
<li><i>pDesc</i> cannot be NULL.
              </li>
</ul>

### -param pDesc

Type: [in, optional] <b>const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a>*</b>

A pointer to a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure that describes the unordered-access view.
          
A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and for buffers UAVs target a full buffer and are typed, and for textures UAVs target the first mip and all array slices. Not all resources support null descriptor initialization.

### -param DestDescriptor [in]

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the unordered-access view.

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
