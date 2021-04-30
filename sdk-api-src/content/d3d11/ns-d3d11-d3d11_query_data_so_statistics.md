---
UID: NS:d3d11.D3D11_QUERY_DATA_SO_STATISTICS
title: D3D11_QUERY_DATA_SO_STATISTICS (d3d11.h)
description: Query information about the amount of data streamed out to the stream-output buffers in between ID3D11DeviceContext::Begin and ID3D11DeviceContext::End.
helpviewer_keywords: ["595165cc-6026-e884-f8d4-b74f4fc8e939","D3D11_QUERY_DATA_SO_STATISTICS","D3D11_QUERY_DATA_SO_STATISTICS structure [Direct3D 11]","d3d11/D3D11_QUERY_DATA_SO_STATISTICS","direct3d11.d3d11_query_data_so_statistics"]
old-location: direct3d11\d3d11_query_data_so_statistics.htm
tech.root: direct3d11
ms.assetid: f5fa2563-817b-4ccd-a2c8-60926fa7d082
ms.date: 12/05/2018
ms.keywords: 595165cc-6026-e884-f8d4-b74f4fc8e939, D3D11_QUERY_DATA_SO_STATISTICS, D3D11_QUERY_DATA_SO_STATISTICS structure [Direct3D 11], d3d11/D3D11_QUERY_DATA_SO_STATISTICS, direct3d11.d3d11_query_data_so_statistics
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
req.typenames: D3D11_QUERY_DATA_SO_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_QUERY_DATA_SO_STATISTICS
 - d3d11/D3D11_QUERY_DATA_SO_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_QUERY_DATA_SO_STATISTICS
---

# D3D11_QUERY_DATA_SO_STATISTICS structure


## -description

Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>.

## -struct-fields

### -field NumPrimitivesWritten

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives (that is, points, lines, and triangles) written to the stream-output buffers.

### -field PrimitivesStorageNeeded

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of primitives that would have been written to the stream-output buffers if there had been enough space for them all.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>