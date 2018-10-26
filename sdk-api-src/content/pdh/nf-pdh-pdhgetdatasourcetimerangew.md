---
UID: NF:pdh.PdhGetDataSourceTimeRangeW
title: PdhGetDataSourceTimeRangeW function
author: windows-sdk-content
description: Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source. To use handles to data sources, use the PdhGetDataSourceTimeRangeH function.
old-location: perf\pdhgetdatasourcetimerange.htm
tech.root: perfctrs
ms.assetid: 142ee829-7f1c-4b97-859c-670f7058dfa1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PdhGetDataSourceTimeRange, PdhGetDataSourceTimeRange function [Perf], PdhGetDataSourceTimeRangeA, PdhGetDataSourceTimeRangeW, _win32_pdhgetdatasourcetimerange, base.pdhgetdatasourcetimerange, pdh/PdhGetDataSourceTimeRange, pdh/PdhGetDataSourceTimeRangeA, pdh/PdhGetDataSourceTimeRangeW, perf.pdhgetdatasourcetimerange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhGetDataSourceTimeRangeW function


## -description


Determines the time range, number of entries and, if applicable, the size of the buffer containing the performance data from the specified input source.
			

To use handles to data sources, use the 
<a href="https://msdn.microsoft.com/55cfef46-999d-43fa-9b09-9d8916fbf755">PdhGetDataSourceTimeRangeH</a> function.


## -parameters




### -param szDataSource [in]

Null-terminated string that specifies the name of a log file from which the time range information is retrieved.


### -param pdwNumEntries [out]

Number of structures in the <i>pInfo</i> buffer. This function collects information for only one time range, so the value is typically 1, or zero if an error occurred. 


### -param pInfo [out]

A 
<a href="https://msdn.microsoft.com/a747f288-8d6c-401c-a927-a61ffea3d423">PDH_TIME_INFO</a> structure that receives the time range.


### -param pdwBufferSize [in]

Size of the <a href="https://msdn.microsoft.com/a747f288-8d6c-401c-a927-a61ffea3d423">PDH_TIME_INFO</a> structure, in bytes.


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




<a href="https://msdn.microsoft.com/55cfef46-999d-43fa-9b09-9d8916fbf755">PdhGetDataSourceTimeRangeH</a>



<a href="https://msdn.microsoft.com/ed0e100e-9f82-48c0-b4bb-72820c5eeaa8">PdhSetQueryTimeRange</a>
 

 

