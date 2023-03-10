---
UID: NS:d3d12.D3D12_VERTEX_BUFFER_VIEW
title: D3D12_VERTEX_BUFFER_VIEW (d3d12.h)
description: Describes a vertex buffer view.
helpviewer_keywords: ["D3D12_VERTEX_BUFFER_VIEW","D3D12_VERTEX_BUFFER_VIEW structure","d3d12/D3D12_VERTEX_BUFFER_VIEW","direct3d12.d3d12_vertex_buffer_view"]
old-location: direct3d12\d3d12_vertex_buffer_view.htm
tech.root: direct3d12
ms.assetid: 7EFE1929-FCDD-48DD-99E4-135D8B515290
ms.date: 12/05/2018
ms.keywords: D3D12_VERTEX_BUFFER_VIEW, D3D12_VERTEX_BUFFER_VIEW structure, d3d12/D3D12_VERTEX_BUFFER_VIEW, direct3d12.d3d12_vertex_buffer_view
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
req.typenames: D3D12_VERTEX_BUFFER_VIEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VERTEX_BUFFER_VIEW
 - d3d12/D3D12_VERTEX_BUFFER_VIEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_VERTEX_BUFFER_VIEW
---

# D3D12_VERTEX_BUFFER_VIEW structure


## -description

Describes a vertex buffer view.

## -struct-fields

### -field BufferLocation

Specifies a D3D12_GPU_VIRTUAL_ADDRESS that identifies the address of the buffer.

### -field SizeInBytes

Specifies the size in bytes of the buffer.

### -field StrideInBytes

Specifies the size in bytes of each vertex entry.

## -remarks

Use this structure with the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers">IASetVertexBuffers</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>