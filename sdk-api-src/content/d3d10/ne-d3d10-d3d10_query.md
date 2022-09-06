---
UID: NE:d3d10.D3D10_QUERY
title: D3D10_QUERY (d3d10.h)
description: Query types.
helpviewer_keywords: ["D3D10_QUERY","D3D10_QUERY enumeration [Direct3D 10]","D3D10_QUERY_EVENT","D3D10_QUERY_OCCLUSION","D3D10_QUERY_OCCLUSION_PREDICATE","D3D10_QUERY_PIPELINE_STATISTICS","D3D10_QUERY_SO_OVERFLOW_PREDICATE","D3D10_QUERY_SO_STATISTICS","D3D10_QUERY_TIMESTAMP","D3D10_QUERY_TIMESTAMP_DISJOINT","d3d10/D3D10_QUERY","d3d10/D3D10_QUERY_EVENT","d3d10/D3D10_QUERY_OCCLUSION","d3d10/D3D10_QUERY_OCCLUSION_PREDICATE","d3d10/D3D10_QUERY_PIPELINE_STATISTICS","d3d10/D3D10_QUERY_SO_OVERFLOW_PREDICATE","d3d10/D3D10_QUERY_SO_STATISTICS","d3d10/D3D10_QUERY_TIMESTAMP","d3d10/D3D10_QUERY_TIMESTAMP_DISJOINT","direct3d10.d3d10_query","e40f5532-bdd2-10c8-b69c-1b328c82ae9c"]
old-location: direct3d10\d3d10_query.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query.htm
ms.date: 12/05/2018
ms.keywords: D3D10_QUERY, D3D10_QUERY enumeration [Direct3D 10], D3D10_QUERY_EVENT, D3D10_QUERY_OCCLUSION, D3D10_QUERY_OCCLUSION_PREDICATE, D3D10_QUERY_PIPELINE_STATISTICS, D3D10_QUERY_SO_OVERFLOW_PREDICATE, D3D10_QUERY_SO_STATISTICS, D3D10_QUERY_TIMESTAMP, D3D10_QUERY_TIMESTAMP_DISJOINT, d3d10/D3D10_QUERY, d3d10/D3D10_QUERY_EVENT, d3d10/D3D10_QUERY_OCCLUSION, d3d10/D3D10_QUERY_OCCLUSION_PREDICATE, d3d10/D3D10_QUERY_PIPELINE_STATISTICS, d3d10/D3D10_QUERY_SO_OVERFLOW_PREDICATE, d3d10/D3D10_QUERY_SO_STATISTICS, d3d10/D3D10_QUERY_TIMESTAMP, d3d10/D3D10_QUERY_TIMESTAMP_DISJOINT, direct3d10.d3d10_query, e40f5532-bdd2-10c8-b69c-1b328c82ae9c
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
req.typenames: D3D10_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_QUERY
 - d3d10/D3D10_QUERY
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
 - D3D10_QUERY
---

# D3D10_QUERY enumeration


## -description

Query types.

## -enum-fields

### -field D3D10_QUERY_EVENT:0

Determines whether or not the GPU is finished processing commands. When the GPU is finished processing commands <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> will return S_OK, and pData will point to a BOOL with a value of <b>TRUE</b>. When using this type of query, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> is disabled.

### -field D3D10_QUERY_OCCLUSION

Get the number of samples that passed the depth and stencil tests in between <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">End</a>. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> returns a UINT64. If a depth or stencil test is disabled, then each of those tests will be counted as a pass.

### -field D3D10_QUERY_TIMESTAMP

Get a timestamp value where <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> returns a UINT64. This kind of query is only useful if two timestamp queries are done in the middle of a D3D10_QUERY_TIMESTAMP_DISJOINT query. The difference of two timestamps can be used to determine how many ticks have elapsed, and the D3D10_QUERY_TIMESTAMP_DISJOINT query will determine if that difference is a reliable value and also has a value that shows how to convert the number of ticks into seconds. See <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_data_timestamp_disjoint">D3D10_QUERY_DATA_TIMESTAMP_DISJOINT</a>. When using this type of query, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> is disabled.

### -field D3D10_QUERY_TIMESTAMP_DISJOINT

Determines whether or not a D3D10_QUERY_TIMESTAMP is returning reliable values, and also gives the frequency of the processor enabling you to convert the number of elapsed ticks into seconds. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> will return a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_data_timestamp_disjoint">D3D10_QUERY_DATA_TIMESTAMP_DISJOINT</a>. This type of query should only be invoked once per frame or less.

### -field D3D10_QUERY_PIPELINE_STATISTICS

Get pipeline statistics, such as the number of pixel shader invocations in between <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">End</a>. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> will return a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_data_pipeline_statistics">D3D10_QUERY_DATA_PIPELINE_STATISTICS</a>.

### -field D3D10_QUERY_OCCLUSION_PREDICATE

Similar to D3D10_QUERY_OCCLUSION, except <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> returns a BOOL indicating whether or not any samples passed the depth and stencil tests - <b>TRUE</b> meaning at least one passed, <b>FALSE</b> meaning none passed.

### -field D3D10_QUERY_SO_STATISTICS

Get streaming output statistics, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">End</a>. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> will return a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_query_data_so_statistics">D3D10_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D10_QUERY_SO_OVERFLOW_PREDICATE

Determines whether or not any of the streaming output buffers overflowed in between <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">End</a>. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
