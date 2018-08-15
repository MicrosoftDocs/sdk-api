---
UID: NS:d3d12.D3D12_QUERY_DATA_PIPELINE_STATISTICS
title: D3D12_QUERY_DATA_PIPELINE_STATISTICS
author: windows-sdk-content
description: Query information about graphics-pipeline activity in between calls to BeginQuery and EndQuery.
old-location: direct3d12\d3d12_query_data_pipeline_statistics.htm
old-project: direct3d12
ms.assetid: 0A84A3C8-0F6F-420E-88C9-26EC03F03179
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_QUERY_DATA_PIPELINE_STATISTICS, D3D12_QUERY_DATA_PIPELINE_STATISTICS structure, d3d12/D3D12_QUERY_DATA_PIPELINE_STATISTICS, direct3d12.d3d12_query_data_pipeline_statistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_QUERY_DATA_PIPELINE_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_QUERY_DATA_PIPELINE_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

