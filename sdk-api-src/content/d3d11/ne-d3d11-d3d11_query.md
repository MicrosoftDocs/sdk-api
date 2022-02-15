---
UID: NE:d3d11.D3D11_QUERY
title: D3D11_QUERY (d3d11.h)
description: Query types.
helpviewer_keywords: ["846a075c-6f8e-9009-e75c-0c3b32d97453","D3D11_QUERY","D3D11_QUERY enumeration [Direct3D 11]","D3D11_QUERY_EVENT","D3D11_QUERY_OCCLUSION","D3D11_QUERY_OCCLUSION_PREDICATE","D3D11_QUERY_PIPELINE_STATISTICS","D3D11_QUERY_SO_OVERFLOW_PREDICATE","D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM0","D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM1","D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM2","D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM3","D3D11_QUERY_SO_STATISTICS","D3D11_QUERY_SO_STATISTICS_STREAM0","D3D11_QUERY_SO_STATISTICS_STREAM1","D3D11_QUERY_SO_STATISTICS_STREAM2","D3D11_QUERY_SO_STATISTICS_STREAM3","D3D11_QUERY_TIMESTAMP","D3D11_QUERY_TIMESTAMP_DISJOINT","d3d11/D3D11_QUERY","d3d11/D3D11_QUERY_EVENT","d3d11/D3D11_QUERY_OCCLUSION","d3d11/D3D11_QUERY_OCCLUSION_PREDICATE","d3d11/D3D11_QUERY_PIPELINE_STATISTICS","d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE","d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM0","d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM1","d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM2","d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM3","d3d11/D3D11_QUERY_SO_STATISTICS","d3d11/D3D11_QUERY_SO_STATISTICS_STREAM0","d3d11/D3D11_QUERY_SO_STATISTICS_STREAM1","d3d11/D3D11_QUERY_SO_STATISTICS_STREAM2","d3d11/D3D11_QUERY_SO_STATISTICS_STREAM3","d3d11/D3D11_QUERY_TIMESTAMP","d3d11/D3D11_QUERY_TIMESTAMP_DISJOINT","direct3d11.d3d11_query"]
old-location: direct3d11\d3d11_query.htm
tech.root: direct3d11
ms.assetid: 4161fbeb-7f58-422c-a195-ea10f737fd0c
ms.date: 12/05/2018
ms.keywords: 846a075c-6f8e-9009-e75c-0c3b32d97453, D3D11_QUERY, D3D11_QUERY enumeration [Direct3D 11], D3D11_QUERY_EVENT, D3D11_QUERY_OCCLUSION, D3D11_QUERY_OCCLUSION_PREDICATE, D3D11_QUERY_PIPELINE_STATISTICS, D3D11_QUERY_SO_OVERFLOW_PREDICATE, D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM0, D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM1, D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM2, D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM3, D3D11_QUERY_SO_STATISTICS, D3D11_QUERY_SO_STATISTICS_STREAM0, D3D11_QUERY_SO_STATISTICS_STREAM1, D3D11_QUERY_SO_STATISTICS_STREAM2, D3D11_QUERY_SO_STATISTICS_STREAM3, D3D11_QUERY_TIMESTAMP, D3D11_QUERY_TIMESTAMP_DISJOINT, d3d11/D3D11_QUERY, d3d11/D3D11_QUERY_EVENT, d3d11/D3D11_QUERY_OCCLUSION, d3d11/D3D11_QUERY_OCCLUSION_PREDICATE, d3d11/D3D11_QUERY_PIPELINE_STATISTICS, d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE, d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM0, d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM1, d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM2, d3d11/D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM3, d3d11/D3D11_QUERY_SO_STATISTICS, d3d11/D3D11_QUERY_SO_STATISTICS_STREAM0, d3d11/D3D11_QUERY_SO_STATISTICS_STREAM1, d3d11/D3D11_QUERY_SO_STATISTICS_STREAM2, d3d11/D3D11_QUERY_SO_STATISTICS_STREAM3, d3d11/D3D11_QUERY_TIMESTAMP, d3d11/D3D11_QUERY_TIMESTAMP_DISJOINT, direct3d11.d3d11_query
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
req.typenames: D3D11_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_QUERY
 - d3d11/D3D11_QUERY
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
 - D3D11_QUERY
---

# D3D11_QUERY enumeration


## -description

Query types.

## -enum-fields

### -field D3D11_QUERY_EVENT:0

Determines whether or not the GPU is finished processing commands. When the GPU is finished processing commands <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return S_OK, and pData will point to a BOOL with a value of <b>TRUE</b>. When using this type of query, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> is disabled.

### -field D3D11_QUERY_OCCLUSION

Get the number of samples that passed the depth and stencil tests in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a UINT64. If a depth or stencil test is disabled, then each of those tests will be counted as a pass.

### -field D3D11_QUERY_TIMESTAMP

Get a timestamp value where <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a UINT64. This kind of query is only useful if two timestamp queries are done in the middle of a D3D11_QUERY_TIMESTAMP_DISJOINT query. The difference of two timestamps can be used to determine how many ticks have elapsed, and the D3D11_QUERY_TIMESTAMP_DISJOINT query will determine if that difference is a reliable value and also has a value that shows how to convert the number of ticks into seconds. See <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_timestamp_disjoint">D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</a>. When using this type of query, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> is disabled.

### -field D3D11_QUERY_TIMESTAMP_DISJOINT

Determines whether or not a D3D11_QUERY_TIMESTAMP is returning reliable values, and also gives the frequency of the processor enabling you to convert the number of elapsed ticks into seconds. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_timestamp_disjoint">D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</a>. This type of query should only be invoked once per frame or less.

### -field D3D11_QUERY_PIPELINE_STATISTICS

Get pipeline statistics, such as the number of pixel shader invocations in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_pipeline_statistics">D3D11_QUERY_DATA_PIPELINE_STATISTICS</a>.

### -field D3D11_QUERY_OCCLUSION_PREDICATE

Similar to D3D11_QUERY_OCCLUSION, except <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL indicating whether or not any samples passed the depth and stencil tests - <b>TRUE</b> meaning at least one passed, <b>FALSE</b> meaning none passed.

### -field D3D11_QUERY_SO_STATISTICS

Get streaming output statistics, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_so_statistics">D3D11_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D11_QUERY_SO_OVERFLOW_PREDICATE

Determines whether or not any of the streaming output buffers overflowed in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

### -field D3D11_QUERY_SO_STATISTICS_STREAM0

Get streaming output statistics for stream 0, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_so_statistics">D3D11_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM0

Determines whether or not the stream 0 output buffers overflowed in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

### -field D3D11_QUERY_SO_STATISTICS_STREAM1

Get streaming output statistics for stream 1, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_so_statistics">D3D11_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM1

Determines whether or not the stream 1 output buffers overflowed in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

### -field D3D11_QUERY_SO_STATISTICS_STREAM2

Get streaming output statistics for stream 2, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_so_statistics">D3D11_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM2

Determines whether or not the stream 2 output buffers overflowed in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

### -field D3D11_QUERY_SO_STATISTICS_STREAM3

Get streaming output statistics for stream 3, such as the number of primitives streamed out in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> will return a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_query_data_so_statistics">D3D11_QUERY_DATA_SO_STATISTICS</a> structure.

### -field D3D11_QUERY_SO_OVERFLOW_PREDICATE_STREAM3

Determines whether or not the stream 3 output buffers overflowed in between <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a>. <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> returns a BOOL - <b>TRUE</b> meaning there was an overflow, <b>FALSE</b> meaning there was not an overflow. If streaming output writes to multiple buffers, and one of the buffers overflows, then it will stop writing to all the output buffers. When an overflow is detected by Direct3D it is prevented from happening - no memory is corrupted. This predication may be used in conjunction with an SO_STATISTICS query so that when an overflow occurs the SO_STATISTIC query will let the application know how much memory was needed to prevent an overflow.

## -remarks

Create a query with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createquery">ID3D11Device::CreateQuery</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
