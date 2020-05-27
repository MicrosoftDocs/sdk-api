---
UID: NF:pdh.PdhBindInputDataSourceA
title: PdhBindInputDataSourceA function (pdh.h)
description: Binds one or more binary log files together for reading log data.
helpviewer_keywords: ["PdhBindInputDataSource","PdhBindInputDataSource function [Perf]","PdhBindInputDataSourceA","PdhBindInputDataSourceW","_win32_pdhbindinputdatasource","base.pdhbindinputdatasource","pdh/PdhBindInputDataSource","pdh/PdhBindInputDataSourceA","pdh/PdhBindInputDataSourceW","perf.pdhbindinputdatasource"]
old-location: perf\pdhbindinputdatasource.htm
tech.root: perfctrs
ms.assetid: eaed9b28-eb09-4123-9317-5d3d50e2d77a
ms.date: 12/05/2018
ms.keywords: PdhBindInputDataSource, PdhBindInputDataSource function [Perf], PdhBindInputDataSourceA, PdhBindInputDataSourceW, _win32_pdhbindinputdatasource, base.pdhbindinputdatasource, pdh/PdhBindInputDataSource, pdh/PdhBindInputDataSourceA, pdh/PdhBindInputDataSourceW, perf.pdhbindinputdatasource
f1_keywords:
- pdh/PdhBindInputDataSource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhBindInputDataSourceA function


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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.




## -remarks



This function is used with the PDH functions that require a handle to a data source. For a list of these functions, see See Also.

You cannot specify more than one comma-delimited (CSV) or tab-delimited (TSV) file. The list can contain only one type of file—you cannot combine multiple file types.

To close the bound log files, call the <a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhcloselog">PdhCloseLog</a> function using the log handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersha">PdhBrowseCountersH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenummachinesha">PdhEnumMachinesH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenumobjectitemsha">PdhEnumObjectItemsH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpathha">PdhExpandWildCardPathH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdatasourcetimerangeh">PdhGetDataSourceTimeRangeH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfcounterha">PdhGetDefaultPerfCounterH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfobjectha">PdhGetDefaultPerfObjectH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenqueryh">PdhOpenQueryH</a>
 

 

