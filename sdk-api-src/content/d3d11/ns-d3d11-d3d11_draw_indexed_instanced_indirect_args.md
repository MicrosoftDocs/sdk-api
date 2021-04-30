---
UID: NS:d3d11.D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
title: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS (d3d11.h)
description: Arguments for draw indexed instanced indirect.
helpviewer_keywords: ["D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS","D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS structure [Direct3D 11]","d3d11/D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS","direct3d11.d3d11_draw_indexed_instanced_indirect_args"]
old-location: direct3d11\d3d11_draw_indexed_instanced_indirect_args.htm
tech.root: direct3d11
ms.assetid: 26530AAB-2E41-4165-AE19-5B8F95AE5A20
ms.date: 12/05/2018
ms.keywords: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS, D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS structure [Direct3D 11], d3d11/D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS, direct3d11.d3d11_draw_indexed_instanced_indirect_args
req.header: d3d11.h
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
req.typenames: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
 - d3d11/D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
---

# D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS structure


## -description

Arguments for draw indexed instanced indirect.

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
          <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstanced">ID3D11DeviceContext::DrawIndexedInstanced</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>