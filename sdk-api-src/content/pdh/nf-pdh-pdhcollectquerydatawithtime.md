---
UID: NF:pdh.PdhCollectQueryDataWithTime
title: PdhCollectQueryDataWithTime function (pdh.h)
description: Collects the current raw data value for all counters in the specified query and updates the status code of each counter. (PdhCollectQueryDataWithTime)
helpviewer_keywords: ["PdhCollectQueryDataWithTime","PdhCollectQueryDataWithTime function [Perf]","base.pdhcollectquerydatawithtime","pdh/PdhCollectQueryDataWithTime","perf.pdhcollectquerydatawithtime"]
old-location: perf\pdhcollectquerydatawithtime.htm
tech.root: perf
ms.assetid: 2c47c690-0748-4ed4-a138-894d45c72581
ms.date: 12/05/2018
ms.keywords: PdhCollectQueryDataWithTime, PdhCollectQueryDataWithTime function [Perf], base.pdhcollectquerydatawithtime, pdh/PdhCollectQueryDataWithTime, perf.pdhcollectquerydatawithtime
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PdhCollectQueryDataWithTime
 - pdh/PdhCollectQueryDataWithTime
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
 - PdhCollectQueryDataWithTime
---

# PdhCollectQueryDataWithTime function


## -description

Collects the current raw data value for all counters in the specified query and updates the status code of each counter.

## -parameters

### -param hQuery [in, out]

Handle of the query for which you want to collect data. The <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle.

### -param pllTimeStamp [out]

Time stamp when the first counter value in the query was retrieved. The time is specified as FILETIME.

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
The query does not currently have any counters.

</td>
</tr>
</table>

## -remarks

Call this function when you want to collect counter data for the counters in the query. PDH stores the raw counter values for the current and previous collection. 

If you want to retrieve the current raw counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>. If the counter path contains a wildcard for the instance name, instead call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcounterarraya">PdhGetRawCounterArray</a> and <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcounterarraya">PdhGetFormattedCounterArray</a> functions, respectively.

When 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydataex">PdhCollectQueryDataEx</a> is called for data from one counter instance only, and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryDataEx</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> or 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a> function for each of the counter instances of interest to determine whether they exist.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>
