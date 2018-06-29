---
UID: NF:pdh.PdhComputeCounterStatistics
title: PdhComputeCounterStatistics function
author: windows-sdk-content
description: Computes statistics for a counter from an array of raw values.
old-location: perf\pdhcomputecounterstatistics.htm
old-project: PerfCtrs
ms.assetid: a986ae6c-88ee-4a03-9077-3d286157b9d1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhComputeCounterStatistics, PdhComputeCounterStatistics function [Perf], _win32_pdhcomputecounterstatistics, base.pdhcomputecounterstatistics, pdh/PdhComputeCounterStatistics, perf.pdhcomputecounterstatistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhComputeCounterStatistics
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhComputeCounterStatistics function


## -description


Computes statistics for a counter from an array of raw values.
		


## -parameters




### -param hCounter [in]

Handle of the counter for which you want to compute statistics. The 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function returns this handle.


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
<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a> structures that contain <i>dwNumEntries</i> entries.


### -param data [out]

A 
<a href="https://msdn.microsoft.com/a1daedfd-55f6-418e-b71f-8334cb628d98">PDH_STATISTICS</a> structure that receives the counter statistics.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

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




<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>



<a href="https://msdn.microsoft.com/a1daedfd-55f6-418e-b71f-8334cb628d98">PDH_STATISTICS</a>



<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>



<a href="https://msdn.microsoft.com/6db99e03-0b03-4c1c-b82a-2982b52746db">PdhSetCounterScaleFactor</a>
 

 

