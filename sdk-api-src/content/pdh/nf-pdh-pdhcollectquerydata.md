---
UID: NF:pdh.PdhCollectQueryData
title: PdhCollectQueryData function (pdh.h)
description: Collects the current raw data value for all counters in the specified query and updates the status code of each counter. (PdhCollectQueryData)
helpviewer_keywords: ["PdhCollectQueryData","PdhCollectQueryData function [Perf]","_win32_pdhcollectquerydata","base.pdhcollectquerydata","pdh/PdhCollectQueryData","perf.pdhcollectquerydata"]
old-location: perf\pdhcollectquerydata.htm
tech.root: perf
ms.assetid: 1d83325b-8deb-4731-9df4-6201da292cdc
ms.date: 12/05/2018
ms.keywords: PdhCollectQueryData, PdhCollectQueryData function [Perf], _win32_pdhcollectquerydata, base.pdhcollectquerydata, pdh/PdhCollectQueryData, perf.pdhcollectquerydata
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
 - PdhCollectQueryData
 - pdh/PdhCollectQueryData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-eventing-pdh-l1-1-3.dll
 - ext-ms-win-eventing-pdh-l1-1-2.dll
 - ext-ms-win-eventing-pdh-l1-1-1.dll
 - ext-ms-win-eventing-pdh-l1-1-0.dll
 - Pdh.dll
api_name:
 - PdhCollectQueryData
---

# PdhCollectQueryData function


## -description

Collects the current raw data value for all counters in the specified query and updates the status code of each counter.

## -parameters

### -param hQuery [in, out]

Handle of the query for which you want to collect data. The <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle.

## -returns

If the function succeeds, it returns ERROR_SUCCESS. Otherwise, the function returns a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.
						
					


The following are possible values.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The query handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The query does not currently contain any counters. The query may not contain data because the user is not running with an elevated token (see <a href="/windows/desktop/PerfCtrs/limited-user-access-support">Limited User Access Support</a>).

</td>
</tr>
</table>

## -remarks

Call this function when you want to collect counter data for the counters in the query. PDH stores the raw counter values for the current and previous collection. 

If you want to retrieve the current raw counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a> function. If the counter path contains a wildcard for the instance name, instead call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcounterarraya">PdhGetRawCounterArray</a> and <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcounterarraya">PdhGetFormattedCounterArray</a> functions, respectively.

When 
<b>PdhCollectQueryData</b> is called for data from one counter instance only and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryData</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> or 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a> for each of the counter instances of interest to determine whether they exist.

The following shows the syntax if calling this function from Visual Basic.


``` syntax
PdhCollectQueryData(
  ByVal QueryHandle as Long  
)
as Long
```




#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/browsing-performance-counters">Browsing Performance Counters</a> or 
<a href="/windows/desktop/PerfCtrs/reading-performance-data-from-a-log-file">Reading Performance Data from a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a>
