---
UID: NS:d3d10.D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
title: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT (d3d10.h)
description: Query information about the reliability of a timestamp query. (D3D10_QUERY_DATA_TIMESTAMP_DISJOINT)
helpviewer_keywords: ["D3D10_QUERY_DATA_TIMESTAMP_DISJOINT","D3D10_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 10]","d3d10/D3D10_QUERY_DATA_TIMESTAMP_DISJOINT","direct3d10.d3d10_query_data_timestamp_disjoint","ecae4d34-b796-887c-40aa-bb10d9b020bf"]
old-location: direct3d10\d3d10_query_data_timestamp_disjoint.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_data_timestamp_disjoint.htm
ms.date: 12/05/2018
ms.keywords: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT, D3D10_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 10], d3d10/D3D10_QUERY_DATA_TIMESTAMP_DISJOINT, direct3d10.d3d10_query_data_timestamp_disjoint, ecae4d34-b796-887c-40aa-bb10d9b020bf
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
req.typenames: D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
 - d3d10/D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
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
 - D3D10_QUERY_DATA_TIMESTAMP_DISJOINT
---

# D3D10_QUERY_DATA_TIMESTAMP_DISJOINT structure


## -description

Query information about the reliability of a timestamp query.

## -struct-fields

### -field Frequency

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

How frequently the GPU counter increments in Hz.

### -field Disjoint

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If this is <b>TRUE</b>, something occurred in between the query's <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a> calls that caused the timestamp counter to become discontinuous or disjoint, such as unplugging the AC chord on a laptop, overheating, or throttling up/down due to laptop savings events. The timestamp returned by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> for a timestamp query is only reliable if Disjoint is <b>FALSE</b>.

## -remarks

For a list of query types see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_query">D3D10_QUERY</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
