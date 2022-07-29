---
UID: NS:d3d12.D3D12_BUFFER_UAV
title: D3D12_BUFFER_UAV (d3d12.h)
description: Describes the elements in a buffer to use in a unordered-access view. (D3D12_BUFFER_UAV)
helpviewer_keywords: ["D3D12_BUFFER_UAV","D3D12_BUFFER_UAV structure","d3d12/D3D12_BUFFER_UAV","direct3d12.d3d12_buffer_uav"]
old-location: direct3d12\d3d12_buffer_uav.htm
tech.root: direct3d12
ms.assetid: 13E48B8F-4EF7-45B7-88F2-61D9BA1801D2
ms.date: 12/05/2018
ms.keywords: D3D12_BUFFER_UAV, D3D12_BUFFER_UAV structure, d3d12/D3D12_BUFFER_UAV, direct3d12.d3d12_buffer_uav
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
req.typenames: D3D12_BUFFER_UAV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUFFER_UAV
 - d3d12/D3D12_BUFFER_UAV
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
 - D3D12_BUFFER_UAV
---

# D3D12_BUFFER_UAV structure


## -description

Describes the elements in a buffer to use in a unordered-access view.

## -struct-fields

### -field FirstElement

The zero-based index of the first element to be accessed.

### -field NumElements

The number of elements in the resource. For structured buffers, this is the number of structures in the buffer.

### -field StructureByteStride

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer.

### -field CounterOffsetInBytes

The counter offset, in bytes.

### -field Flags

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags">D3D12_BUFFER_UAV_FLAGS</a>-typed value that specifies the view options for the resource.

## -remarks

Use this structure with a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure to view the resource as a buffer.

If <i>StructureByteStride</i> value is not 0, a view of a structured buffer is created and the D3D12_UNORDERED_ACCESS_VIEW_DESC::Format field must be DXGI_FORMAT_UNKNOWN. If <i>StructureByteStride</i> is 0, a typed view of a buffer is created and a format must be supplied. The specified format for the typed view must be supported by the hardware. More information on this topic can be found in the <a href="/en-gb/windows/win32/direct3d12/typed-unordered-access-view-loads">Typed unordered access view (UAV) loads</a> page.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>

<a href="/en-gb/windows/win32/direct3d12/typed-unordered-access-view-loads">Typed unordered access view (UAV) loads</a>
