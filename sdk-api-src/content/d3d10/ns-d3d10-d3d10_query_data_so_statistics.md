---
UID: NS:d3d10.D3D10_QUERY_DATA_SO_STATISTICS
title: D3D10_QUERY_DATA_SO_STATISTICS (d3d10.h)
description: Query information about the amount of data streamed out to the stream-output buffers in between ID3D10Asynchronous::Begin and ID3D10Asynchronous::End.
helpviewer_keywords: ["D3D10_QUERY_DATA_SO_STATISTICS","D3D10_QUERY_DATA_SO_STATISTICS structure [Direct3D 10]","cf410b92-83dc-df50-69b8-4970b24d4f1c","d3d10/D3D10_QUERY_DATA_SO_STATISTICS","direct3d10.d3d10_query_data_so_statistics"]
old-location: direct3d10\d3d10_query_data_so_statistics.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_so_statistics.htm
ms.date: 12/05/2018
ms.keywords: D3D10_QUERY_DATA_SO_STATISTICS, D3D10_QUERY_DATA_SO_STATISTICS structure [Direct3D 10], cf410b92-83dc-df50-69b8-4970b24d4f1c, d3d10/D3D10_QUERY_DATA_SO_STATISTICS, direct3d10.d3d10_query_data_so_statistics
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
req.typenames: D3D10_QUERY_DATA_SO_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_QUERY_DATA_SO_STATISTICS
 - d3d10/D3D10_QUERY_DATA_SO_STATISTICS
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
 - D3D10_QUERY_DATA_SO_STATISTICS
---

# D3D10_QUERY_DATA_SO_STATISTICS structure


## -description

Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a>.

## -struct-fields

### -field NumPrimitivesWritten

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives (that is, points, lines, and triangles) written to the stream-output buffers.

### -field PrimitivesStorageNeeded

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives that would have been written to the stream-output buffers if there had been enough space for them all.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>