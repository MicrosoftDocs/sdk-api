---
UID: NF:pdh.PdhGetFormattedCounterValue
title: PdhGetFormattedCounterValue function
author: windows-sdk-content
description: Computes a displayable value for the specified counter.
old-location: perf\pdhgetformattedcountervalue.htm
old-project: perfctrs
ms.assetid: cd104b26-1498-4f95-a411-97d868b43836
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PDH_FMT_1000, PDH_FMT_DOUBLE, PDH_FMT_LARGE, PDH_FMT_LONG, PDH_FMT_NOCAP100, PDH_FMT_NOSCALE, PdhGetFormattedCounterValue, PdhGetFormattedCounterValue function [Perf], _win32_pdhgetformattedcountervalue, base.pdhgetformattedcountervalue, pdh/PdhGetFormattedCounterValue, perf.pdhgetformattedcountervalue
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
 - PdhGetFormattedCounterValue
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhGetFormattedCounterValue function


## -description



			Computes a displayable value for the specified counter.
		


## -parameters




### -param hCounter [in]

Handle of the counter for which you want to compute a displayable value. The 
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
Return data as a double-precision floating point real.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_LARGE"></a><a id="pdh_fmt_large"></a><dl>
<dt><b>PDH_FMT_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Return data as a 64-bit integer.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_FMT_LONG"></a><a id="pdh_fmt_long"></a><dl>
<dt><b>PDH_FMT_LONG</b></dt>
</dl>
</td>
<td width="60%">
Return data as a long integer.

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
Do not apply the counter's default scaling factor.

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
Multiply the actual value by 1,000.

</td>
</tr>
</table>
 


### -param lpdwType [out]

Receives the counter type. For a list of counter types, see the Counter Types section of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84422">Windows Server 2003 Deployment Kit</a>. This parameter is optional.


### -param pValue [out]

A 
<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure that receives the counter value.


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
A parameter is not valid or is incorrectly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified counter does not contain valid data or a successful status code.

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



The data for the counter is locked (protected) for the duration of the call to 
<b>PdhGetFormattedCounterValue</b> to prevent any changes during the processing of the call. Reading the data (calling this function successfully) clears the data-changed flag for the counter.

Some counters, such as rate counters, require two counter values in order to compute a displayable value. In this case you must call <a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a> twice before calling 
<b>PdhGetFormattedCounterValue</b>. For more information, see <a href="https://msdn.microsoft.com/2534d387-a280-4716-9a9d-3e42f40e2f92">Collecting Performance Data</a>. 

If 
the specified counter instance does not exist, the method will return PDH_INVALID_DATA and set the <b>CStatus</b> member of the 
<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure to PDH_CSTATUS_NO_INSTANCE.

<b>Prior to Windows Server 2003:  </b>The format call may fail for counters that require only a single value when the instance is not found. Try calling the query and format calls again. If the format call fails the second time, the instance is not found. As an alternative, you can call the <a href="https://msdn.microsoft.com/dfa4b10f-5134-4620-a6b0-0fa2c13a33ec">PdhEnumObjects</a> function with the refresh option set to <b>TRUE</b> to refresh the counter instances before querying and formatting the counter data.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/44c5cfa8-6449-45d8-ac30-979b99c086de">Browsing Performance Counters</a> or 
<a href="https://msdn.microsoft.com/acec1506-473a-43c9-9b57-ad8c00e8f250">Reading Performance Data from a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>



<a href="https://msdn.microsoft.com/6db99e03-0b03-4c1c-b82a-2982b52746db">PdhSetCounterScaleFactor</a>
 

 

