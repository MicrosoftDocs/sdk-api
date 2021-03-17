---
UID: NF:pdh.PdhGetDataSourceTimeRangeH
title: PdhGetDataSourceTimeRangeH function (pdh.h)
description: Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source.This function is identical to the PdhGetDataSourceTimeRange function, except that it supports the use of handles to data sources.
helpviewer_keywords: ["PdhGetDataSourceTimeRangeH","PdhGetDataSourceTimeRangeH function [Perf]","_win32_pdhgetdatasourcetimerangeh","base.pdhgetdatasourcetimerangeh","pdh/PdhGetDataSourceTimeRangeH","perf.pdhgetdatasourcetimerangeh"]
old-location: perf\pdhgetdatasourcetimerangeh.htm
tech.root: perf
ms.assetid: 55cfef46-999d-43fa-9b09-9d8916fbf755
ms.date: 12/05/2018
ms.keywords: PdhGetDataSourceTimeRangeH, PdhGetDataSourceTimeRangeH function [Perf], _win32_pdhgetdatasourcetimerangeh, base.pdhgetdatasourcetimerangeh, pdh/PdhGetDataSourceTimeRangeH, perf.pdhgetdatasourcetimerangeh
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
 - PdhGetDataSourceTimeRangeH
 - pdh/PdhGetDataSourceTimeRangeH
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
 - PdhGetDataSourceTimeRangeH
---

# PdhGetDataSourceTimeRangeH function


## -description

Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source.

This function is identical to 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangea">PdhGetDataSourceTimeRange</a> function, except that it supports the use of handles to data sources.

## -parameters

### -param hDataSource [in]

Handle to a data source returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.

### -param pdwNumEntries [out]

Number of structures in the <i>pInfo</i> buffer. This function collects information for only one time range, so the value is typically 1, or zero if an error occurred.

### -param pInfo [out]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_time_info">PDH_TIME_INFO</a> structure that receives the time range. The information spans all bound log files.

### -param pdwBufferSize [in]

Size of the <a href="/windows/desktop/api/pdh/ns-pdh-pdh_time_info">PDH_TIME_INFO</a> structure, in bytes.

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
<tr>
<td width="40%">
<dl>
<dt><b>PDH_DATA_SOURCE_IS_REAL_TIME</b></dt>
</dl>
</td>
<td width="60%">
The current data source is a real-time data source.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>