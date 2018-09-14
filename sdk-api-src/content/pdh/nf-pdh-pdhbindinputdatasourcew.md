---
UID: NF:pdh.PdhBindInputDataSourceW
title: PdhBindInputDataSourceW function
author: windows-sdk-content
description: Binds one or more binary log files together for reading log data.
old-location: perf\pdhbindinputdatasource.htm
tech.root: PerfCtrs
ms.assetid: eaed9b28-eb09-4123-9317-5d3d50e2d77a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PdhBindInputDataSource, PdhBindInputDataSource function [Perf], PdhBindInputDataSourceA, PdhBindInputDataSourceW, _win32_pdhbindinputdatasource, base.pdhbindinputdatasource, pdh/PdhBindInputDataSource, pdh/PdhBindInputDataSourceA, pdh/PdhBindInputDataSourceW, perf.pdhbindinputdatasource
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
req.unicode-ansi: PdhBindInputDataSourceW (Unicode) and PdhBindInputDataSourceA (ANSI)
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
 - PdhBindInputDataSource
 - PdhBindInputDataSourceA
 - PdhBindInputDataSourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhBindInputDataSourceW function


## -description


Binds one or more binary log files together for reading log data.
		


## -parameters




### -param phDataSource [out]

Handle to the bound data sources.


### -param LogFileNameList [in]

<b>Null</b>-terminated string that contains one or more binary log files to bind together. Terminate each log file name with a <b>null</b>-terminator character and the list with one additional <b>null</b>-terminator character. The log file names can contain absolute or relative paths. You cannot specify more than 32 log files.

If <b>NULL</b>, the source is a real-time data source.


## -returns



Returns ERROR_SUCCESS if the function succeeds.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.




## -remarks



This function is used with the PDH functions that require a handle to a data source. For a list of these functions, see See Also.

You cannot specify more than one comma-delimited (CSV) or tab-delimited (TSV) file. The list can contain only one type of file—you cannot combine multiple file types.

To close the bound log files, call the <a href="https://msdn.microsoft.com/74039bdf-d1b5-41ba-aa4e-4779ce0dd02a">PdhCloseLog</a> function using the log handle.




## -see-also




<a href="https://msdn.microsoft.com/ab835bf8-1adc-463f-99c3-654a328af98a">PdhBrowseCountersH</a>



<a href="https://msdn.microsoft.com/7e8dc113-76a7-4a7a-bbad-1a4387831501">PdhEnumMachinesH</a>



<a href="https://msdn.microsoft.com/2cea7d0a-cea2-4fee-a087-37663de254e9">PdhEnumObjectItemsH</a>



<a href="https://msdn.microsoft.com/8f68a7a8-cc56-4f7f-a86f-4b439738808d">PdhEnumObjectsH</a>



<a href="https://msdn.microsoft.com/d7d13beb-02ab-4204-808e-d395197f09e1">PdhExpandWildCardPathH</a>



<a href="https://msdn.microsoft.com/55cfef46-999d-43fa-9b09-9d8916fbf755">PdhGetDataSourceTimeRangeH</a>



<a href="https://msdn.microsoft.com/d1b3de9a-99ab-4339-8e9f-906f5a5d291d">PdhGetDefaultPerfCounterH</a>



<a href="https://msdn.microsoft.com/4950d5b7-3a6f-410d-830f-7868aa84f6d5">PdhGetDefaultPerfObjectH</a>



<a href="https://msdn.microsoft.com/068c55da-d7e0-4111-91c8-a2bbd676f99d">PdhOpenQueryH</a>
 

 

