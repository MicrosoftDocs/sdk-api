---
UID: NS:d3d12.D3D12_QUERY_DATA_SO_STATISTICS
title: D3D12_QUERY_DATA_SO_STATISTICS (d3d12.h)
description: Describes query data for stream output.
helpviewer_keywords: ["D3D12_QUERY_DATA_SO_STATISTICS","D3D12_QUERY_DATA_SO_STATISTICS structure","d3d12/D3D12_QUERY_DATA_SO_STATISTICS","direct3d12.d3d12_query_data_so_statistics"]
old-location: direct3d12\d3d12_query_data_so_statistics.htm
tech.root: direct3d12
ms.assetid: 7A71F6DA-AAC2-4070-90E9-F91F090AD1A1
ms.date: 12/05/2018
req.header: d3d12.h
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
req.typenames: D3D12_QUERY_DATA_SO_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_QUERY_DATA_SO_STATISTICS
 - d3d12/D3D12_QUERY_DATA_SO_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_QUERY_DATA_SO_STATISTICS
---

## -description

Describes query data about the amount of data streamed out to the stream-output buffers.

## -struct-fields

### -field NumPrimitivesWritten

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

The number of primitives (that is, points, lines, and triangles) that were actually written to the stream output resource.

### -field PrimitivesStorageNeeded

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

If the stream output resource is large enough, then *PrimitivesStorageNeeded* represents the total number of primitives written to the stream output resource. Otherwise, it represents the total number of primitives that *would* have been written to the stream-output resource had there been enough space for them all.

## -remarks

Use this structure with [D3D12_QUERY_HEAP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) and [CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

## -see-also

* [Core structures](/windows/win32/direct3d12/direct3d-12-structures)
