---
UID: NS:d3d10.D3D10_QUERY_DATA_PIPELINE_STATISTICS
title: D3D10_QUERY_DATA_PIPELINE_STATISTICS
author: windows-sdk-content
description: Query information about graphics-pipeline activity in between calls to ID3D10Asynchronous::Begin and ID3D10Asynchronous::End.
old-location: direct3d10\d3d10_query_data_pipeline_statistics.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_pipeline_statistics.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 0f1e36bb-cb67-6e39-ddb2-784ed615c5bb, D3D10_QUERY_DATA_PIPELINE_STATISTICS, D3D10_QUERY_DATA_PIPELINE_STATISTICS structure [Direct3D 10], d3d10/D3D10_QUERY_DATA_PIPELINE_STATISTICS, direct3d10.d3d10_query_data_pipeline_statistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
tech.root: 
req.typenames: D3D10_QUERY_DATA_PIPELINE_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_DATA_PIPELINE_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_QUERY_DATA_PIPELINE_STATISTICS structure


## -description


Query information about graphics-pipeline activity in between calls to <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">ID3D10Asynchronous::End</a>.


## -struct-fields




### -field IAVertices

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of vertices read by input assembler.


### -field IAPrimitives

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives read by the input assembler. This number can be different depending on the primitive topology used. For example, a triangle strip with 6 vertices will produce 4 triangles, however a triangle list with 6 vertices will produce 2 triangles. 


### -field VSInvocations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of times a vertex shader was invoked. Direct3D invokes the vertex shader once per vertex.


### -field GSInvocations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of times a geometry shader was invoked. When the geometry shader is set to <b>NULL</b>, this statistic may or may not increment depending on the hardware manufacturer.


### -field GSPrimitives

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives output by a geometry shader.


### -field CInvocations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives that were sent to the rasterizer. When the rasterizer is disabled, this will not increment.


### -field CPrimitives

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of primitives that were rendered. This may be larger or smaller than CInvocations because after a primitive is clipped sometimes it is either broken up into more than one primitive or completely culled.


### -field PSInvocations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of times a pixel shader was invoked.


## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

