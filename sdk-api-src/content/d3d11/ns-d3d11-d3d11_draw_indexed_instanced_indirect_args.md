---
UID: NS:d3d11.D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
title: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
author: windows-sdk-content
description: Arguments for draw indexed instanced indirect.
old-location: direct3d11\d3d11_draw_indexed_instanced_indirect_args.htm
tech.root: direct3d11
ms.assetid: 26530AAB-2E41-4165-AE19-5B8F95AE5A20
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS, D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS structure [Direct3D 11], d3d11/D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS, direct3d11.d3d11_draw_indexed_instanced_indirect_args
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
product: Windows
targetos: Windows
req.typenames: D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS
req.redist: 
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
          <a href="https://msdn.microsoft.com/c7a4821a-324c-47e4-b89f-603d2afcfb51">ID3D11DeviceContext::DrawIndexedInstanced</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

