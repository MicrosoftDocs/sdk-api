---
UID: NS:d3d11.D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
title: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT (d3d11.h)
description: Query information about the reliability of a timestamp query. (D3D11_QUERY_DATA_TIMESTAMP_DISJOINT)
helpviewer_keywords: ["D3D11_QUERY_DATA_TIMESTAMP_DISJOINT","D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 11]","d3d11/D3D11_QUERY_DATA_TIMESTAMP_DISJOINT","direct3d11.d3d11_query_data_timestamp_disjoint","f6339efd-3b83-c410-71de-6ecde51119d9"]
old-location: direct3d11\d3d11_query_data_timestamp_disjoint.htm
tech.root: direct3d11
ms.assetid: d706626a-cf11-4087-b66a-350161050aad
ms.date: 12/05/2018
ms.keywords: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT, D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure [Direct3D 11], d3d11/D3D11_QUERY_DATA_TIMESTAMP_DISJOINT, direct3d11.d3d11_query_data_timestamp_disjoint, f6339efd-3b83-c410-71de-6ecde51119d9
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
req.typenames: D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
 - d3d11/D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
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
 - D3D11_QUERY_DATA_TIMESTAMP_DISJOINT
---

# D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure


## -description

Query information about the reliability of a timestamp query.

## -struct-fields

### -field Frequency

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

How frequently the GPU counter increments in Hz.

### -field Disjoint

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If this is <b>TRUE</b>, something occurred in between the query's <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> calls that caused the timestamp counter to become discontinuous or disjoint, such as unplugging the AC cord on a laptop, overheating, or throttling up/down due to laptop savings events. The timestamp returned by <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> for a timestamp query is only reliable if <b>Disjoint</b> is <b>FALSE</b>.

## -remarks

For a list of query types see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
