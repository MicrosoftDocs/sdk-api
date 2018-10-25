---
UID: NS:perflib._PERF_COUNTER_HEADER
title: "_PERF_COUNTER_HEADER"
author: windows-sdk-content
description: Contains information about the PERF_COUNTER_HEADER block that contains the structure.
old-location: perf\perf_counter_header.htm
tech.root: perfctrs
ms.assetid: 8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PPERF_COUNTER_HEADER, PERF_COUNTERSET, PERF_COUNTER_HEADER, PERF_COUNTER_HEADER structure [Perf], PERF_ERROR_RETURN, PERF_MULTIPLE_COUNTERS, PERF_MULTIPLE_INSTANCES, PERF_SINGLE_COUNTER, PPERF_COUNTER_HEADER, PPERF_COUNTER_HEADER structure pointer [Perf], _PERF_COUNTER_HEADER, perf.perf_counter_header, perflib/PERF_COUNTER_HEADER, perflib/PPERF_COUNTER_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTER_HEADER
product: Windows
targetos: Windows
req.typenames: PERF_COUNTER_HEADER, *PPERF_COUNTER_HEADER
req.redist: 
---

# _PERF_COUNTER_HEADER structure


## -description


Contains information about the <b>PERF_COUNTER_HEADER</b> block that contains the structure. A <b>PERF_COUNTER_HEADER</b> block provides error information and data for performance counter queries, and consists of a <b>PERF_COUNTER_HEADER</b> structure
followed by additional performance counter data.


## -struct-fields




### -field dwStatus

 An error code that indicates whether the operation to query the performance succeeded or failed.



### -field dwType

The type of performance counter information that the <b>PERF_COUNTER_HEADER</b> block provides.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_ERROR_RETURN"></a><a id="perf_error_return"></a><dl>
<dt><b>PERF_ERROR_RETURN</b></dt>
</dl>
</td>
<td width="60%">
An error that was the result of a performance counter query. The performance library cannot get valid counter data back from provider.
  No additional data follows the <b>PERF_COUNTER_HEADER</b> structure. The <b>dwStatus</b> member of the structure
  contains the error code.



</td>
</tr>
<tr>
<td width="40%"><a id="PERF_SINGLE_COUNTER"></a><a id="perf_single_counter"></a><dl>
<dt><b>PERF_SINGLE_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
The result of a  single-counter, single-instance query; for example,
  "\Processor(_Total)\% Processor Time". The additional data consists of a <a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a> block.



</td>
</tr>
<tr>
<td width="40%"><a id="PERF_MULTIPLE_COUNTERS"></a><a id="perf_multiple_counters"></a><dl>
<dt><b>PERF_MULTIPLE_COUNTERS</b></dt>
</dl>
</td>
<td width="60%">
The result of a  multi-counter, single-instance query; for example, "\Processor(_Total)\*". The additional data consists of a <a href="https://msdn.microsoft.com/4F490C3C-F587-4E7B-B316-162EDA76EC30">PERF_MULTI_COUNTERS</a> block followed by  <a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a> blocks.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_MULTIPLE_INSTANCES"></a><a id="perf_multiple_instances"></a><dl>
<dt><b>PERF_MULTIPLE_INSTANCES</b></dt>
</dl>
</td>
<td width="60%">
The result of a single-counter, multi-instance query; for example, "\Processor(*)\% Processor Time". The additional data consists of a <a href="https://msdn.microsoft.com/5EC34ECD-D240-4B44-A52B-C5518918400C">PERF_MULTI_INSTANCES</a> block.



</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET"></a><a id="perf_counterset"></a><dl>
<dt><b>PERF_COUNTERSET</b></dt>
</dl>
</td>
<td width="60%">
The result of a multi-counter, multi-instance query; for example,
  "\Processor(*)\*". The additional data consists of a 
  <a href="https://msdn.microsoft.com/4F490C3C-F587-4E7B-B316-162EDA76EC30">PERF_MULTI_COUNTERS</a> block followed by a <a href="https://msdn.microsoft.com/5EC34ECD-D240-4B44-A52B-C5518918400C">PERF_MULTI_INSTANCES</a> block.

</td>
</tr>
</table>
 


### -field dwSize

The total size of the <b>PERF_COUNTER_HEADER</b> block, which equals the sum of the size of the <b>PERF_COUNTER_HEADER</b> structure and the size of the  additional data.


### -field Reserved

Reserved.


## -remarks



The <a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a> function returns a <a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a> block that
contains a sequence of <b>PERF_COUNTER_HEADER</b> blocks.




## -see-also




<a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a>



<a href="https://msdn.microsoft.com/4F490C3C-F587-4E7B-B316-162EDA76EC30">PERF_MULTI_COUNTERS</a>



<a href="https://msdn.microsoft.com/5EC34ECD-D240-4B44-A52B-C5518918400C">PERF_MULTI_INSTANCES</a>



<a href="https://msdn.microsoft.com/E64C73F0-034E-408B-8537-CE6855C01347">PerfCounterDataType</a>
 

 

