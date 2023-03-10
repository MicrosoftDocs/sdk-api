---
UID: NS:d3d12.D3D12_DRAW_INDEXED_ARGUMENTS
title: D3D12_DRAW_INDEXED_ARGUMENTS (d3d12.h)
description: Describes parameters for drawing indexed instances.
helpviewer_keywords: ["D3D12_DRAW_INDEXED_ARGUMENTS","D3D12_DRAW_INDEXED_ARGUMENTS structure","d3d12/D3D12_DRAW_INDEXED_ARGUMENTS","direct3d12.d3d12_draw_indexed_arguments"]
old-location: direct3d12\d3d12_draw_indexed_arguments.htm
tech.root: direct3d12
ms.assetid: FD26CA56-B430-4019-B8F6-DC8981126692
ms.date: 12/05/2018
ms.keywords: D3D12_DRAW_INDEXED_ARGUMENTS, D3D12_DRAW_INDEXED_ARGUMENTS structure, d3d12/D3D12_DRAW_INDEXED_ARGUMENTS, direct3d12.d3d12_draw_indexed_arguments
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
req.typenames: D3D12_DRAW_INDEXED_ARGUMENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DRAW_INDEXED_ARGUMENTS
 - d3d12/D3D12_DRAW_INDEXED_ARGUMENTS
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
 - D3D12_DRAW_INDEXED_ARGUMENTS
---

# D3D12_DRAW_INDEXED_ARGUMENTS structure


## -description

Describes parameters for drawing indexed instances.

## -struct-fields

### -field IndexCountPerInstance

The number of indices read from the index buffer for each instance.

### -field InstanceCount

 The number of instances to draw.

### -field StartIndexLocation

The location of the first index read by the GPU from the index buffer.

### -field BaseVertexLocation

A value added to each index before reading a vertex from the vertex buffer.

### -field StartInstanceLocation

 A value added to each index before reading per-instance data from a vertex buffer.

## -remarks

The members of this structure serve the same purpose as the parameters of
          <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced">DrawIndexedInstanced</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>