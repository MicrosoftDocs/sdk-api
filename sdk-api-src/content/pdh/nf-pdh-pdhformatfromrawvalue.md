---
UID: NF:pdh.PdhFormatFromRawValue
title: PdhFormatFromRawValue function (pdh.h)
description: Computes a displayable value for the given raw counter values.
helpviewer_keywords: ["PDH_FMT_1000","PDH_FMT_DOUBLE","PDH_FMT_LARGE","PDH_FMT_LONG","PDH_FMT_NOCAP100","PDH_FMT_NOSCALE","PdhFormatFromRawValue","PdhFormatFromRawValue function [Perf]","_win32_pdhformatfromrawvalue","base.pdhformatfromrawvalue","pdh/PdhFormatFromRawValue","perf.pdhformatfromrawvalue"]
old-location: perf\pdhformatfromrawvalue.htm
tech.root: perf
ms.assetid: 13027af4-2e76-4c2f-88e8-a2554a16fae3
ms.date: 12/05/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhFormatFromRawValue, PdhFormatFromRawValue function [Perf], _win32_pdhformatfromrawvalue, base.pdhformatfromrawvalue, pdh/PdhFormatFromRawValue, perf.pdhformatfromrawvalue
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
 - PdhFormatFromRawValue
 - pdh/PdhFormatFromRawValue
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
 - PdhFormatFromRawValue
---

# PdhFormatFromRawValue function


## -description

Computes a displayable value for the given raw counter values.

## -parameters

### -param dwCounterType [in]

Type of counter. Typically, you call <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a> to retrieve the counter type at the time you call <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> to retrieve the raw counter value.

For a list of counter types, see the Counter Types section of the <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Windows Server 2003 Deployment Kit</a>. (The constant values are defined in Winperf.h.)

Note that you cannot specify base types, for example, PERF_LARGE_RAW_BASE.

### -param dwFormat [in]

Determines the data type of the calculated value. Specify one of the following values. 



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
Do not apply the counter's scaling factor in the calculation.

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

### -param pTimeBase [in]

Pointer to the time base, if necessary for the format conversion. If time base information is not necessary for the format conversion, the value of this parameter is ignored. To retrieve the time base of the counter, call <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcountertimebase">PdhGetCounterTimeBase</a>.

### -param pRawValue1 [in]

Raw counter value used to compute the displayable counter value. For details, see <a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a>.

### -param pRawValue2 [in]

Raw counter value used to compute the displayable counter value. For details, see <a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a>. Some counters, for example, rate counters, require two raw values to calculate a displayable value. If the counter type does not require a second value, set this parameter to <b>NULL</b>. This value must be the older of the two raw values.

### -param pFmtValue [out]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_fmt_countervalue">PDH_FMT_COUNTERVALUE</a> structure that receives the calculated counter value.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_fmt_countervalue">PDH_FMT_COUNTERVALUE</a>



<a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcountertimebase">PdhGetCounterTimeBase</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhreadrawlogrecord">PdhReadRawLogRecord</a>