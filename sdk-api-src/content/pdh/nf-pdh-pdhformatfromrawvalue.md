---
UID: NF:pdh.PdhFormatFromRawValue
title: PdhFormatFromRawValue function (pdh.h)
author: windows-sdk-content
description: Computes a displayable value for the given raw counter values.
old-location: perf\pdhformatfromrawvalue.htm
tech.root: perfctrs
ms.assetid: 13027af4-2e76-4c2f-88e8-a2554a16fae3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhFormatFromRawValue, PdhFormatFromRawValue function [Perf], _win32_pdhformatfromrawvalue, base.pdhformatfromrawvalue, pdh/PdhFormatFromRawValue, perf.pdhformatfromrawvalue
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhFormatFromRawValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhFormatFromRawValue function


## -description


Computes a displayable value for the given raw counter values.
		


## -parameters




### -param dwCounterType [in]

Type of counter. Typically, you call <a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> to retrieve the counter type at the time you call <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> to retrieve the raw counter value.

For a list of counter types, see the Counter Types section of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84422">Windows Server 2003 Deployment Kit</a>. (The constant values are defined in Winperf.h.)

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

Pointer to the time base, if necessary for the format conversion. If time base information is not necessary for the format conversion, the value of this parameter is ignored. To retrieve the time base of the counter, call <a href="https://msdn.microsoft.com/b034c00e-50f1-46af-aebc-0cb968c0b737">PdhGetCounterTimeBase</a>.


### -param pRawValue1 [in]

Raw counter value used to compute the displayable counter value. For details, see <a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>. 


### -param pRawValue2 [in]

Raw counter value used to compute the displayable counter value. For details, see <a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>. Some counters, for example, rate counters, require two raw values to calculate a displayable value. If the counter type does not require a second value, set this parameter to <b>NULL</b>. This value must be the older of the two raw values.


### -param pFmtValue [out]

A 
<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure that receives the calculated counter value.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. 




## -see-also




<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a>



<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>



<a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a>



<a href="https://msdn.microsoft.com/b034c00e-50f1-46af-aebc-0cb968c0b737">PdhGetCounterTimeBase</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>



<a href="https://msdn.microsoft.com/fb93b6ea-ca31-4ff1-a553-b02388be8b72">PdhReadRawLogRecord</a>
 

 

