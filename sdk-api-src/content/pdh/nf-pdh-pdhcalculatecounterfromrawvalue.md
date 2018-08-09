---
UID: NF:pdh.PdhCalculateCounterFromRawValue
title: PdhCalculateCounterFromRawValue function
author: windows-sdk-content
description: Calculates the displayable value of two raw counter values.
old-location: perf\pdhcalculatecounterfromrawvalue.htm
old-project: PerfCtrs
ms.assetid: fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhCalculateCounterFromRawValue, PdhCalculateCounterFromRawValue function [Perf], _win32_pdhcalculatecounterfromrawvalue, base.pdhcalculatecounterfromrawvalue, pdh/PdhCalculateCounterFromRawValue, perf.pdhcalculatecounterfromrawvalue
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
 - PdhCalculateCounterFromRawValue
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhCalculateCounterFromRawValue function


## -description


Calculates the displayable value of two raw counter values.
		


## -parameters




### -param hCounter [in]

Handle to the counter to calculate. The function uses information from the counter to determine how to calculate the value. This handle is returned by the 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function.


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
 


### -param rawValue1 [in]

Raw counter value used to compute the displayable counter value. For details, see the <a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a> structure. 


### -param rawValue2 [in]

Raw counter value used to compute the displayable counter value. For details, see <a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>. Some counters (for example, rate counters) require two raw values to calculate a displayable value. If the counter type does not require a second value, set this parameter to <b>NULL</b>. This value must be the older of the two raw values.


### -param fmtValue [out]

A 
<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure that receives the calculated counter value.


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
 




## -remarks



To retrieve the current raw counter value from the query, call the <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> function.




## -see-also




<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a>



<a href="https://msdn.microsoft.com/237a3c82-0ab4-45cb-bd93-2f308178c573">PDH_RAW_COUNTER</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>



<a href="https://msdn.microsoft.com/6db99e03-0b03-4c1c-b82a-2982b52746db">PdhSetCounterScaleFactor</a>
 

 

