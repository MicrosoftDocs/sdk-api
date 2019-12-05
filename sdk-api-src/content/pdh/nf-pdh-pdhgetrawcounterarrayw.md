---
UID: NF:pdh.PdhGetRawCounterArrayW
title: PdhGetRawCounterArrayW function (pdh.h)
description: Returns an array of raw values from the specified counter. Use this function when you want to retrieve the raw counter values of a counter that contains a wildcard character for the instance name.
old-location: perf\pdhgetrawcounterarray.htm
tech.root: perfctrs
ms.assetid: 03b30d08-6901-45cd-bd6d-d2672eb0f914
ms.date: 12/05/2018
ms.keywords: PdhGetRawCounterArray, PdhGetRawCounterArray function [Perf], PdhGetRawCounterArrayA, PdhGetRawCounterArrayW, _win32_pdhgetrawcounterarray, base.pdhgetrawcounterarray, pdh/PdhGetRawCounterArray, pdh/PdhGetRawCounterArrayA, pdh/PdhGetRawCounterArrayW, perf.pdhgetrawcounterarray
ms.topic: function
f1_keywords:
- pdh/PdhGetRawCounterArray
dev_langs:
- c++
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhGetRawCounterArrayW (Unicode) and PdhGetRawCounterArrayA (ANSI)
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
- PdhGetRawCounterArray
- PdhGetRawCounterArrayA
- PdhGetRawCounterArrayW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhGetRawCounterArrayW function


## -description


Returns an array of raw values from the specified counter.
		Use this function when you want to retrieve the raw counter values of a counter that contains a wildcard character for the instance name.
		


## -parameters




### -param hCounter [in]

Handle of the counter for whose current raw instance values you want to retrieve. The 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.


### -param lpdwBufferSize [in, out]

Size of the <i>ItemBuffer</i> buffer, in bytes. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.


### -param lpdwItemCount [out]

Number of raw counter values in the <i>ItemBuffer</i> buffer.


### -param ItemBuffer [out]

Caller-allocated buffer that receives the array of 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter_item_a">PDH_RAW_COUNTER_ITEM</a> structures; the structures contain the raw instance counter values.  Set to <b>NULL</b> if <i>lpdwBufferSize</i> is zero.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>ItemBuffer</i> buffer is not large enough to contain the object name. This return value is expected if <i>lpdwBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid or is incorrectly formatted. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

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



You should call this function twice, the first time to get the required buffer size (set <i>ItemBuffer</i> to <b>NULL</b> and <i>lpdwBufferSize</i> to 0), and the second time to get the data.

The data for the counter is locked for the duration of the call to 
<b>PdhGetRawCounterArray</b> to prevent any changes during processing of the call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter_item_a">PDH_RAW_COUNTER_ITEM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcounterarraya">PdhGetFormattedCounterArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>
 

 

