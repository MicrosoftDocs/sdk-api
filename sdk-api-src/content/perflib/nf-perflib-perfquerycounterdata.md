---
UID: NF:perflib.PerfQueryCounterData
title: PerfQueryCounterData function (perflib.h)
description: Gets the values of the performance counters that match the counter specifications in the specified query.
helpviewer_keywords: ["PerfQueryCounterData","PerfQueryCounterData function [Perf]","perf.perfquerycounterdata","perflib/PerfQueryCounterData"]
old-location: perf\perfquerycounterdata.htm
tech.root: perf
ms.assetid: EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC
ms.date: 12/05/2018
ms.keywords: PerfQueryCounterData, PerfQueryCounterData function [Perf], perf.perfquerycounterdata, perflib/PerfQueryCounterData
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
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfQueryCounterData
 - perflib/PerfQueryCounterData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-perf-legacy-l1-1-0.dll
 - AdvAPI32.dll
api_name:
 - PerfQueryCounterData
---

# PerfQueryCounterData function


## -description

Gets the values of the performance counters that match the counter specifications in the
specified query.

## -parameters

### -param hQuery [in]

A handle to a query for the counter specifications of the performance counters for which you want to get the values.

### -param pCounterBlock [out, optional]

A pointer to a buffer that has enough space to receive the amount of  data that the <i>cbCounterBlock</i> parameter specifies, in bytes. May be NULL if  

<i>cbCounterBlock</i> is 0.

### -param cbCounterBlock

The size of the buffer that the <i>pCounterBlock</i> parameter specifies, in bytes.

### -param pcbCounterBlockActual [out]

The size of the buffer actually required to get the performance counter values. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcbCounterBlockActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  bytes of performance counter values that the function stored in the buffer that <i>pCounterBlock</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size of the buffer required to store the performance counter values, in bytes. Enlarge the buffer to the required  

  size and call the function again.  

</td>
</tr>
<tr>
<td>Other</td>
<td>The value is undefined and should not be used.</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function successfully stored all of the requested performance counter values in the buffer that <i>pCounterBlock</i> specified. The value that <i>pcbCounterBlockActual</i> points to indicates amount of information actually stored in the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pCounterBlock</i> specified was not large enough to store all of the requested performance counter values.  The value that <i>pcbCounterBlockActual</i> points to  indicates the size of the buffer required to store all of the information. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 

For other types of failures, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The information about the performance counter values is  written to the buffer that <i>pCounterBlock</i> specifies as a <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block, which consists <b>PERF_DATA_HEADER</b> structure followed by a sequence of <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> blocks.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a>