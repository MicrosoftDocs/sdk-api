---
UID: NF:pdh.PdhComputeCounterStatistics
title: PdhComputeCounterStatistics function (pdh.h)
description: Computes statistics for a counter from an array of raw values.
helpviewer_keywords: ["PDH_FMT_1000","PDH_FMT_DOUBLE","PDH_FMT_LARGE","PDH_FMT_LONG","PDH_FMT_NOCAP100","PDH_FMT_NOSCALE","PdhComputeCounterStatistics","PdhComputeCounterStatistics function [Perf]","_win32_pdhcomputecounterstatistics","base.pdhcomputecounterstatistics","pdh/PdhComputeCounterStatistics","perf.pdhcomputecounterstatistics"]
old-location: perf\pdhcomputecounterstatistics.htm
tech.root: perf
ms.assetid: a986ae6c-88ee-4a03-9077-3d286157b9d1
ms.date: 12/05/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhComputeCounterStatistics, PdhComputeCounterStatistics function [Perf], _win32_pdhcomputecounterstatistics, base.pdhcomputecounterstatistics, pdh/PdhComputeCounterStatistics, perf.pdhcomputecounterstatistics
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhComputeCounterStatistics
 - pdh/PdhComputeCounterStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhComputeCounterStatistics
---

# PdhComputeCounterStatistics function


## -description

Computes statistics for a counter from an array of raw values.

## -parameters

### -param hCounter [in]

Handle of the counter for which you want to compute statistics. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.

### -param dwFormat [in]

Determines the data type of the formatted value. Specify one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_DOUBLE"></a><a id="pdh_fmt_double"></a><dl>
<dt><b>PDH_FMT_DOUBLE</b></dt>
</dl>
</td>
<td width="60%">
Return the calculated value as a double-precision floating point real.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_LARGE"></a><a id="pdh_fmt_large"></a><dl>
<dt><b>PDH_FMT_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Return the calculated value as a 64-bit integer.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_LONG"></a><a id="pdh_fmt_long"></a><dl>
<dt><b>PDH_FMT_LONG</b></dt>
</dl>
</td>
<td width="60%">
Return the calculated value as a long integer.

</td>
</tr>
</table>
 

You can use the bitwise inclusive OR operator (|) to combine the data type with one of the following scaling factors.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_NOSCALE"></a><a id="pdh_fmt_noscale"></a><dl>
<dt><b>PDH_FMT_NOSCALE</b></dt>
</dl>
</td>
<td width="60%">
Do not apply the counter's scaling factors in the calculation.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_NOCAP100"></a><a id="pdh_fmt_nocap100"></a><dl>
<dt><b>PDH_FMT_NOCAP100</b></dt>
</dl>
</td>
<td width="60%">
Counter values greater than 100 (for example, counter values measuring the processor load on multiprocessor computers) will not be reset to 100. The default behavior is that counter values are capped at a value of 100.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_1000"></a><a id="pdh_fmt_1000"></a><dl>
<dt><b>PDH_FMT_1000</b></dt>
</dl>
</td>
<td width="60%">
Multiply the final value by 1,000.

</td>
</tr>
</table>

### -param dwFirstEntry [in]

Zero-based index of the first raw counter value to use to begin the calculations. The index value must point to the oldest entry in the buffer. The 
function starts at this entry and scans through the buffer, wrapping at the last entry back to the beginning of the buffer and up to the <i>dwFirstEntry-1</i> entry, which is assumed to be the newest or most recent data.

### -param dwNumEntries [in]

Number of raw counter values in the <i>lpRawValueArray</i> buffer.

### -param lpRawValueArray [in]

Array of 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a> structures that contain <i>dwNumEntries</i> entries.

### -param data [out]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_statistics">PDH_STATISTICS</a> structure that receives the counter statistics.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
An argument is not correct or is incorrectly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The counter handle is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a>



<a href="/windows/desktop/api/pdh/ns-pdh-pdh_statistics">PDH_STATISTICS</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhsetcounterscalefactor">PdhSetCounterScaleFactor</a>