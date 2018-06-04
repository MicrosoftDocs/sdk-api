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

# D3D12_QUERY_DATA_PIPELINE_STATISTICS structure


## -description


Query information about graphics-pipeline activity in between calls to <a href="https://msdn.microsoft.com/38011ED8-C867-4ECE-880F-3963A17790F7">BeginQuery</a> and <a href="https://msdn.microsoft.com/591B277C-44C7-4C21-86B1-239F6A71308D">EndQuery</a>.


## -struct-fields




### -field IAVertices

Number of vertices read by input assembler.



### -field IAPrimitives

Number of primitives read by the input assembler. This number can be different depending on the primitive topology used. For example, a triangle strip with 6 vertices will produce 4 triangles, however a triangle list with 6 vertices will produce 2 triangles. 


### -field VSInvocations

Specifies the number of vertex shader invocations. Direct3D invokes the vertex shader once per vertex.


### -field GSInvocations

Specifies the number of geometry shader invocations. When the geometry shader is set to NULL, this statistic may or may not increment depending on the graphics adapter.


### -field GSPrimitives

Specifies the number of geometry shader output primitives.


### -field CInvocations

Number of primitives that were sent to the rasterizer. When the rasterizer is disabled, this will not increment.



### -field CPrimitives

Number of primitives that were rendered. This may be larger or smaller than CInvocations because after a primitive is clipped sometimes it is either broken up into more than one primitive or completely culled.


### -field PSInvocations

Specifies the number of pixel shader invocations.


### -field HSInvocations

Specifies the number of hull shader invocations.


### -field DSInvocations

Specifies the number of domain shader invocations.


### -field CSInvocations

Specifies the number of compute shader invocations.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/FDD5F81B-F356-49D9-B6FE-FE2847934E61">D3D12_QUERY_HEAP_TYPE</a> and <a href="https://msdn.microsoft.com/98B238D0-8E4D-46C1-AC2C-09473A972E71">CreateQueryHeap</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

