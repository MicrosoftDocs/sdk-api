---
UID: NF:pdh.PdhGetRawCounterValue
title: PdhGetRawCounterValue function (pdh.h)
description: Returns the current raw value of the counter.
helpviewer_keywords: ["PdhGetRawCounterValue","PdhGetRawCounterValue function [Perf]","_win32_pdhgetrawcountervalue","base.pdhgetrawcountervalue","pdh/PdhGetRawCounterValue","perf.pdhgetrawcountervalue"]
old-location: perf\pdhgetrawcountervalue.htm
tech.root: perf
ms.assetid: bb246c82-8748-4e2f-9f44-a206199aff90
ms.date: 12/05/2018
ms.keywords: PdhGetRawCounterValue, PdhGetRawCounterValue function [Perf], _win32_pdhgetrawcountervalue, base.pdhgetrawcountervalue, pdh/PdhGetRawCounterValue, perf.pdhgetrawcountervalue
f1_keywords:
- pdh/PdhGetRawCounterValue
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
- PdhGetRawCounterValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhGetRawCounterValue function


## -description


Returns the current raw value of the counter.
		


## -parameters




### -param hCounter [in]

Handle of the counter from which to retrieve the current raw value. The 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.


### -param lpdwType [out]

Receives the counter type. For a list of counter types, see the Counter Types section of the <a href="https://technet.microsoft.com/library/3fb01419-b1ab-4f52-a9f8-09d5ebeb9ef2">Windows Server 2003 Deployment Kit</a>. This parameter is optional.


### -param pValue [out]

A 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a> structure that receives the counter value.


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
<b>PdhGetRawCounterValue</b> to prevent any changes during processing of the call.

If 
the specified counter instance does not exist, this function will return ERROR_SUCCESS and the <b>CStatus</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/ns-pdh-pdh_raw_counter">PDH_RAW_COUNTER</a> structure will contain PDH_CSTATUS_NO_INSTANCE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>
 

 

