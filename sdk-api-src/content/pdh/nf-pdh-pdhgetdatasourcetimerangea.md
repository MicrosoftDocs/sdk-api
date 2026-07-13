---
UID: NF:pdh.PdhGetDataSourceTimeRangeA
title: PdhGetDataSourceTimeRangeA function (pdh.h)
description: Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source. To use handles to data sources, use the PdhGetDataSourceTimeRangeH function. (ANSI)
helpviewer_keywords: ["PdhGetDataSourceTimeRangeA", "pdh/PdhGetDataSourceTimeRangeA"]
old-location: perf\pdhgetdatasourcetimerange.htm
tech.root: perf
ms.assetid: 142ee829-7f1c-4b97-859c-670f7058dfa1
ms.date: 12/05/2018
ms.keywords: PdhGetDataSourceTimeRange, PdhGetDataSourceTimeRange function [Perf], PdhGetDataSourceTimeRangeA, PdhGetDataSourceTimeRangeW, _win32_pdhgetdatasourcetimerange, base.pdhgetdatasourcetimerange, pdh/PdhGetDataSourceTimeRange, pdh/PdhGetDataSourceTimeRangeA, pdh/PdhGetDataSourceTimeRangeW, perf.pdhgetdatasourcetimerange
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhGetDataSourceTimeRangeW (Unicode) and PdhGetDataSourceTimeRangeA (ANSI)
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
 - PdhGetDataSourceTimeRangeA
 - pdh/PdhGetDataSourceTimeRangeA
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
 - PdhGetDataSourceTimeRange
 - PdhGetDataSourceTimeRangeA
 - PdhGetDataSourceTimeRangeW
---

# PdhGetDataSourceTimeRangeA function


## -description

Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangeh">PdhGetDataSourceTimeRangeH</a> function.

## -parameters

### -param szDataSource [in]

Null-terminated string that specifies the name of a log file from which the time range information is retrieved.

### -param pdwNumEntries [out]

Number of structures in the <i>pInfo</i> buffer. This function collects information for only one time range, so the value is typically 1, or zero if an error occurred.

### -param pInfo [out]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_time_info">PDH_TIME_INFO</a> structure that receives the time range.

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

<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangeh">PdhGetDataSourceTimeRangeH</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhsetquerytimerange">PdhSetQueryTimeRange</a>

## -remarks

> [!NOTE]
> The pdh.h header defines PdhGetDataSourceTimeRange as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
