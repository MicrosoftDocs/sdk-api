---
UID: NS:d3d10.D3D10_QUERY_DATA_PIPELINE_STATISTICS
title: D3D10_QUERY_DATA_PIPELINE_STATISTICS (d3d10.h)
description: Query information about graphics-pipeline activity in between calls to ID3D10Asynchronous::Begin and ID3D10Asynchronous::End.
helpviewer_keywords: ["0f1e36bb-cb67-6e39-ddb2-784ed615c5bb","D3D10_QUERY_DATA_PIPELINE_STATISTICS","D3D10_QUERY_DATA_PIPELINE_STATISTICS structure [Direct3D 10]","d3d10/D3D10_QUERY_DATA_PIPELINE_STATISTICS","direct3d10.d3d10_query_data_pipeline_statistics"]
old-location: direct3d10\d3d10_query_data_pipeline_statistics.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_pipeline_statistics.htm
ms.date: 12/05/2018
ms.keywords: 0f1e36bb-cb67-6e39-ddb2-784ed615c5bb, D3D10_QUERY_DATA_PIPELINE_STATISTICS, D3D10_QUERY_DATA_PIPELINE_STATISTICS structure [Direct3D 10], d3d10/D3D10_QUERY_DATA_PIPELINE_STATISTICS, direct3d10.d3d10_query_data_pipeline_statistics
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_QUERY_DATA_PIPELINE_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_QUERY_DATA_PIPELINE_STATISTICS
 - d3d10/D3D10_QUERY_DATA_PIPELINE_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_DATA_PIPELINE_STATISTICS
---

# D3D10_QUERY_DATA_PIPELINE_STATISTICS structure


## -description

Query information about graphics-pipeline activity in between calls to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a>.

## -struct-fields

### -field IAVertices

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of vertices read by input assembler.

### -field IAPrimitives

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives read by the input assembler. This number can be different depending on the primitive topology used. For example, a triangle strip with 6 vertices will produce 4 triangles, however a triangle list with 6 vertices will produce 2 triangles.

### -field VSInvocations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of times a vertex shader was invoked. Direct3D invokes the vertex shader once per vertex.

### -field GSInvocations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of times a geometry shader was invoked. When the geometry shader is set to <b>NULL</b>, this statistic may or may not increment depending on the hardware manufacturer.

### -field GSPrimitives

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives output by a geometry shader.

### -field CInvocations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives that were sent to the rasterizer. When the rasterizer is disabled, this will not increment.

### -field CPrimitives

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives that were rendered. This may be larger or smaller than CInvocations because after a primitive is clipped sometimes it is either broken up into more than one primitive or completely culled.

### -field PSInvocations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of times a pixel shader was invoked.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>