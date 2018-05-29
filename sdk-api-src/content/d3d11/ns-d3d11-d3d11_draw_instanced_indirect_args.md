---
UID: NS:d3d11.D3D11_DRAW_INSTANCED_INDIRECT_ARGS
title: D3D11_DRAW_INSTANCED_INDIRECT_ARGS
author: windows-sdk-content
description: Arguments for draw instanced indirect.
old-location: direct3d11\d3d11_draw_instanced_indirect_args.htm
old-project: direct3d11
ms.assetid: B83B9D3C-3C64-4F42-A08A-4276F09DA9EC
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_DRAW_INSTANCED_INDIRECT_ARGS, D3D11_DRAW_INSTANCED_INDIRECT_ARGS structure [Direct3D 11], d3d11/D3D11_DRAW_INSTANCED_INDIRECT_ARGS, direct3d11.d3d11_draw_instanced_indirect_args
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
req.typenames: D3D11_DRAW_INSTANCED_INDIRECT_ARGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_DRAW_INSTANCED_INDIRECT_ARGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
          <a href="https://msdn.microsoft.com/3cb608e7-d64d-42cc-9b34-5f6c30af2ada">ID3D11DeviceContext::DrawInstanced</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

