---
UID: NF:d3d10.ID3D10Asynchronous.GetData
title: ID3D10Asynchronous::GetData (d3d10.h)
description: Get data from the GPU asynchronously.
helpviewer_keywords: ["GetData","GetData method [Direct3D 10]","GetData method [Direct3D 10]","ID3D10Asynchronous interface","ID3D10Asynchronous interface [Direct3D 10]","GetData method","ID3D10Asynchronous.GetData","ID3D10Asynchronous::GetData","c544fd10-336c-a120-6147-34aee4afeb45","d3d10/ID3D10Asynchronous::GetData","direct3d10.id3d10asynchronous_getdata"]
old-location: direct3d10\id3d10asynchronous_getdata.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10asynchronous_getdata.htm
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Direct3D 10], GetData method [Direct3D 10],ID3D10Asynchronous interface, ID3D10Asynchronous interface [Direct3D 10],GetData method, ID3D10Asynchronous.GetData, ID3D10Asynchronous::GetData, c544fd10-336c-a120-6147-34aee4afeb45, d3d10/ID3D10Asynchronous::GetData, direct3d10.id3d10asynchronous_getdata
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Asynchronous::GetData
 - d3d10/ID3D10Asynchronous::GetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Asynchronous.GetData
---

# ID3D10Asynchronous::GetData


## -description

Get data from the GPU asynchronously.

## -parameters

### -param pData [out]

Type: <b>void*</b>

Address of memory that will receive the data. If <b>NULL</b>, <b>GetData</b> will be used only to check status. The type of data output depends on the type of asynchronous interface. See Remarks.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data to retrieve or 0. This value can be obtained with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdatasize">ID3D10Asynchronous::GetDataSize</a>. Must be 0 when <i>pData</i> is <b>NULL</b>.

### -param GetDataFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional flags. Can be 0 or any combination of the flags enumerated by
            <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_async_getdata_flag">D3D10_ASYNC_GETDATA_FLAG</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns S_OK. Otherwise, possible 
          return values are the following:

<ul>
<li>S_FALSE</li>
<li>DXGI_ERROR_DEVICE_REMOVED</li>
<li>DXGI_ERROR_INVALID_CALL</li>
</ul>

## -remarks

<b>GetData</b> retrieves the data collected between calls to <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a>.  Certain queries only require a call to <b>ID3D10Asynchronous::End</b> in which case the data returned by <b>GetData</b> is accurate up to the last call to <b>ID3D10Asynchronous::End</b> (See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10query">ID3D10Query Interface</a>).

If <i>DataSize</i> is 0, <b>GetData</b> is only used to check status where a return value of S_OK indicates that data is available to give to an application, and a return value of S_FALSE indicates data is not yet available.

It is invalid to invoke this function on a predicate created with the flag D3D10_QUERY_MISCFLAG_PREDICATEHINT.

If the asynchronous interface that calls this function is <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10query">ID3D10Query Interface</a>, then the following table applies.

<table>
<tr>
<th>Query Type</th>
<th>Output Data Type</th>
<th>Supports Begin Method</th>
</tr>
<tr>
<td>D3D10_QUERY_EVENT</td>
<td>BOOL</td>
<td>NO</td>
</tr>
<tr>
<td>D3D10_QUERY_OCCLUSION</td>
<td>UINT64</td>
<td>YES</td>
</tr>
<tr>
<td>D3D10_QUERY_TIMESTAMP</td>
<td>UINT64</td>
<td>NO</td>
</tr>
<tr>
<td>D3D10_QUERY_TIMESTAMP_DISJOINT</td>
<td>D3D10_QUERY_DATA_TIMESTAMP_DISJOINT</td>
<td>YES</td>
</tr>
<tr>
<td>D3D10_QUERY_PIPELINE_STATISTICS</td>
<td>D3D10_QUERY_DATA_PIPELINE_STATISTICS</td>
<td>YES</td>
</tr>
<tr>
<td>D3D10_QUERY_OCCLUSION_PREDICATE</td>
<td>BOOL</td>
<td>YES</td>
</tr>
<tr>
<td>D3D10_QUERY_SO_STATISTICS</td>
<td>D3D10_QUERY_DATA_SO_STATISTICS</td>
<td>YES</td>
</tr>
<tr>
<td>D3D10_QUERY_SO_OVERFLOW_PREDICATE</td>
<td>BOOL</td>
<td>YES</td>
</tr>
</table>
 

If the asynchronous interface that calls this API is <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10counter">ID3D10Counter Interface</a>, then the following applies.

<table>
<tr>
<th>Counter Type</th>
<th>Output Data Type</th>
<th>Units</th>
</tr>
<tr>
<td>D3D10_COUNTER_GPU_IDLE</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_VERTEX_PROCESSING</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_GEOMETRY_PROCESSING</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_PIXEL_PROCESSING</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_OTHER_GPU_PROCESSING</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_HOST_ADAPTER_BANDWIDTH_UTILIZATION</td>
<td>FLOAT32</td>
<td>fraction of theoretical maximum</td>
</tr>
<tr>
<td>D3D10_COUNTER_LOCAL_VIDMEM_BANDWIDTH_UTILIZATION</td>
<td>FLOAT32</td>
<td>fraction of theoretical maximum</td>
</tr>
<tr>
<td>D3D10_COUNTER_VERTEX_THROUGHPUT_UTILIZATION</td>
<td>FLOAT32</td>
<td>fraction of theoretical maximum</td>
</tr>
<tr>
<td>D3D10_COUNTER_TRIANGLE_SETUP_THROUGHPUT_UTILIZATION</td>
<td>FLOAT32</td>
<td>fraction of theoretical maximum</td>
</tr>
<tr>
<td>D3D10_COUNTER_FILLRATE_THROUGHPUT_UTILIZATION</td>
<td>FLOAT32</td>
<td>fraction of theoretical maximum</td>
</tr>
<tr>
<td>D3D10_COUNTER_VS_MEMORY_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_VS_COMPUTATION_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_GS_MEMORY_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_GS_COMPUTATION_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_PS_MEMORY_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_PS_COMPUTATION_LIMITED</td>
<td>FLOAT32</td>
<td>fraction of time</td>
</tr>
<tr>
<td>D3D10_COUNTER_POST_TRANSFORM_CACHE_HIT_RATE</td>
<td>FLOAT32</td>
<td>fraction</td>
</tr>
<tr>
<td>D3D10_COUNTER_TEXTURE_CACHE_HIT_RATE</td>
<td>FLOAT32</td>
<td>fraction</td>
</tr>
</table>
 

The value returned by a D3D10_COUNTER_GPU_IDLE, D3D10_COUNTER_VERTEX_PROCESSING, D3D10_COUNTER_GEOMETRY_PROCESSING, D3D10_COUNTER_PIXEL_PROCESSING, or D3D10_COUNTER_OTHER_GPU_PROCESSING counter may be different depending on the number of parallel counters that exist on a video card, and those values can be interpreted with the following equation:

<img alt="Equation to interpret the number of parallel counters" src="./images/parallelUnits.jpg"/>

The number of parallel counters that a video card has is available from <b>NumDetectableParallelUnits</b> in <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_counter_info">D3D10_COUNTER_INFO</a>, and it can be retrieved by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounterinfo">ID3D10Device::CheckCounterInfo</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous Interface</a>