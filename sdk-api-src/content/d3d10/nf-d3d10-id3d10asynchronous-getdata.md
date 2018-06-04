---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D10Asynchronous::GetData


## -description


Get data from the GPU asynchronously.


## -parameters




### -param pData [out]

Type: <b>void*</b>

Address of memory that will receive the data. If <b>NULL</b>, <b>GetData</b> will be used only to check status. The type of data output depends on the type of asynchronous interface. See Remarks.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the data to retrieve or 0. This value can be obtained with <a href="https://msdn.microsoft.com/1572c6a8-4c77-4cda-95bd-bffdf81a71dd">ID3D10Asynchronous::GetDataSize</a>. Must be 0 when <i>pData</i> is <b>NULL</b>.


### -param GetDataFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional flags. Can be 0 or any combination of the flags enumerated by
            <a href="https://msdn.microsoft.com/6c4ebfbb-00cc-4c2a-b186-fbef395da355">D3D10_ASYNC_GETDATA_FLAG</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns S_OK. Otherwise, possible 
          return values are the following:

<ul>
<li>S_FALSE</li>
<li>DXGI_ERROR_DEVICE_REMOVED</li>
<li>DXGI_ERROR_INVALID_CALL</li>
</ul>



## -remarks



<b>GetData</b> retrieves the data collected between calls to <a href="https://msdn.microsoft.com/53ae44d0-822b-4fc9-ac77-814ac73eb08a">ID3D10Asynchronous::Begin</a> and <a href="https://msdn.microsoft.com/147a93b4-7151-4800-8aa5-286058f49ee8">ID3D10Asynchronous::End</a>.  Certain queries only require a call to <b>ID3D10Asynchronous::End</b> in which case the data returned by <b>GetData</b> is accurate up to the last call to <b>ID3D10Asynchronous::End</b> (See <a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query Interface</a>).

If <i>DataSize</i> is 0, <b>GetData</b> is only used to check status where a return value of S_OK indicates that data is available to give to an application, and a return value of S_FALSE indicates data is not yet available.

It is invalid to invoke this function on a predicate created with the flag D3D10_QUERY_MISCFLAG_PREDICATEHINT.

If the asynchronous interface that calls this function is <a href="https://msdn.microsoft.com/ffa69b76-ce8d-4386-b0be-fecada85d37c">ID3D10Query Interface</a>, then the following table applies.

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
 

If the asynchronous interface that calls this API is <a href="https://msdn.microsoft.com/1844b30a-27fb-415a-9ac8-93d159e9774e">ID3D10Counter Interface</a>, then the following applies.

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

<img alt="Equation to interpret the number of parallel counters" src="images/parallelUnits.jpg"/>

The number of parallel counters that a video card has is available from <b>NumDetectableParallelUnits</b> in <a href="https://msdn.microsoft.com/7df1d574-4660-4249-90b9-03933449be84">D3D10_COUNTER_INFO</a>, and it can be retrieved by calling <a href="https://msdn.microsoft.com/dfa4cc61-2c1d-45a7-839c-f7df64d488ac">ID3D10Device::CheckCounterInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/71ed9ae8-d1a1-442c-ac0f-6b4ede613bfb">ID3D10Asynchronous Interface</a>
 

 

