---
UID: NF:pdh.PdhSetQueryTimeRange
title: PdhSetQueryTimeRange function (pdh.h)
description: Limits the samples that you can read from a log file to those within the specified time range, inclusively.
helpviewer_keywords: ["PdhSetQueryTimeRange","PdhSetQueryTimeRange function [Perf]","_win32_pdhsetquerytimerange","base.pdhsetquerytimerange","pdh/PdhSetQueryTimeRange","perf.pdhsetquerytimerange"]
old-location: perf\pdhsetquerytimerange.htm
tech.root: perf
ms.assetid: ed0e100e-9f82-48c0-b4bb-72820c5eeaa8
ms.date: 12/05/2018
ms.keywords: PdhSetQueryTimeRange, PdhSetQueryTimeRange function [Perf], _win32_pdhsetquerytimerange, base.pdhsetquerytimerange, pdh/PdhSetQueryTimeRange, perf.pdhsetquerytimerange
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
 - PdhSetQueryTimeRange
 - pdh/PdhSetQueryTimeRange
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
 - PdhSetQueryTimeRange
---

# PdhSetQueryTimeRange function


## -description

Limits the samples that you can read from a log file to those within the specified time range, inclusively.

## -parameters

### -param hQuery [in]

Handle to the query. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle.

### -param pInfo [in]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_time_info">PDH_TIME_INFO</a> structure that specifies the time range. Specify the time as local file time. The end time must be greater than the start time. You can specify 0 for the start time and the maximum 64-bit value for the end time if you want to read all records.

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
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The ending time range value must be greater than the starting time range value.

</td>
</tr>
</table>

## -remarks

When the end of the specified time range or the end of the log file is reached, the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a> function will return PDH_NO_MORE_DATA.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangea">PdhGetDataSourceTimeRange</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>