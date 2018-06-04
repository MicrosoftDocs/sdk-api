---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

