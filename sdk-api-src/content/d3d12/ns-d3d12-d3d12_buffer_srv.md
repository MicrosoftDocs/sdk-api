---
UID: NS:d3d12.D3D12_BUFFER_SRV
title: D3D12_BUFFER_SRV (d3d12.h)
description: Describes the elements in a buffer resource to use in a shader-resource view.
helpviewer_keywords: ["D3D12_BUFFER_SRV","D3D12_BUFFER_SRV structure","d3d12/D3D12_BUFFER_SRV","direct3d12.d3d12_buffer_srv"]
old-location: direct3d12\d3d12_buffer_srv.htm
tech.root: direct3d12
ms.assetid: FD5FBA65-4C70-487F-8D93-0EC5668BCE4A
ms.date: 12/05/2018
ms.keywords: D3D12_BUFFER_SRV, D3D12_BUFFER_SRV structure, d3d12/D3D12_BUFFER_SRV, direct3d12.d3d12_buffer_srv
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
req.typenames: D3D12_BUFFER_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUFFER_SRV
 - d3d12/D3D12_BUFFER_SRV
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
 - D3D12_BUFFER_SRV
---

# D3D12_BUFFER_SRV structure

## -description

Describes the elements in a buffer resource to use in a shader-resource view.

## -struct-fields

### -field FirstElement

The index of the first element to be accessed by the view.

### -field NumElements

The number of elements in the resource.

### -field StructureByteStride

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer.  The size must match the struct size declared in shaders that access the view.

### -field Flags

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags">D3D12_BUFFER_SRV_FLAGS</a>-typed value that identifies view options for the buffer. Currently, the only option is to identify a raw view of the buffer. For more info about raw viewing of buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Raw Views of Buffers</a>.

## -remarks

This structure is used by <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a> to create a view of a buffer. 

If the value of *StructureByteStride* is not 0, then a view of a structured buffer is created, and then the *D3D12_SHADER_RESOURCE_VIEW_DESC::Format* field must be **DXGI_FORMAT_UNKNOWN**. If *StructureByteStride* is 0, then a typed view of a buffer is created, and then a format must be supplied. The specified format for the typed view must be supported by the hardware.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
