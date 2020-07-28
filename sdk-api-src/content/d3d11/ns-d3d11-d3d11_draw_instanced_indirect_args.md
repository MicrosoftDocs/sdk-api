---
UID: NS:d3d11.D3D11_DRAW_INSTANCED_INDIRECT_ARGS
title: D3D11_DRAW_INSTANCED_INDIRECT_ARGS (d3d11.h)
description: Arguments for draw instanced indirect.
helpviewer_keywords: ["D3D11_DRAW_INSTANCED_INDIRECT_ARGS","D3D11_DRAW_INSTANCED_INDIRECT_ARGS structure [Direct3D 11]","d3d11/D3D11_DRAW_INSTANCED_INDIRECT_ARGS","direct3d11.d3d11_draw_instanced_indirect_args"]
old-location: direct3d11\d3d11_draw_instanced_indirect_args.htm
tech.root: direct3d11
ms.assetid: B83B9D3C-3C64-4F42-A08A-4276F09DA9EC
ms.date: 12/05/2018
ms.keywords: D3D11_DRAW_INSTANCED_INDIRECT_ARGS, D3D11_DRAW_INSTANCED_INDIRECT_ARGS structure [Direct3D 11], d3d11/D3D11_DRAW_INSTANCED_INDIRECT_ARGS, direct3d11.d3d11_draw_instanced_indirect_args
f1_keywords:
- d3d11/D3D11_DRAW_INSTANCED_INDIRECT_ARGS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d11.h
api_name:
- D3D11_DRAW_INSTANCED_INDIRECT_ARGS
targetos: Windows
req.typenames: D3D11_DRAW_INSTANCED_INDIRECT_ARGS
req.redist: 
ms.custom: 19H1
---

# D3D11_DRAW_INSTANCED_INDIRECT_ARGS structure


## -description


Arguments for draw instanced indirect.
        


## -struct-fields




### -field VertexCountPerInstance

The number of vertices to draw.
          


### -field InstanceCount

The number of instances to draw.
          


### -field StartVertexLocation

The index of the first vertex.
          


### -field StartInstanceLocation

A value added to each index before reading per-instance data from a vertex buffer.
          


## -remarks



The members of this structure serve the same purpose as the parameters of
          <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstanced">ID3D11DeviceContext::DrawInstanced</a>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
 

 

