---
UID: NS:pdh._PDH_TIME_INFO
title: "_PDH_TIME_INFO"
author: windows-sdk-content
description: The PDH_TIME_INFO structure contains information on time intervals as applied to the sampling of performance data.
old-location: perf\pdh_time_info_str.htm
tech.root: perfctrs
ms.assetid: a747f288-8d6c-401c-a927-a61ffea3d423
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PPDH_TIME_INFO, PDH_TIME_INFO, PDH_TIME_INFO structure [Perf], PPDH_TIME_INFO, PPDH_TIME_INFO structure pointer [Perf], _PDH_TIME_INFO, _win32_pdh_time_info_str, base.pdh_time_info_str, pdh/PDH_TIME_INFO, pdh/PPDH_TIME_INFO, perf.pdh_time_info_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_TIME_INFO
product: Windows
targetos: Windows
req.typenames: PDH_TIME_INFO, *PPDH_TIME_INFO
req.redist: 
---

# _PDH_TIME_INFO structure


## -description


The 
<b>PDH_TIME_INFO</b> structure contains information on time intervals as applied to the sampling of performance data.
		


## -struct-fields




### -field StartTime

Starting time of the sample interval, in local <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.
					


### -field EndTime

Ending time of the sample interval, in local <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format.


### -field SampleCount

Number of samples collected during the interval.


## -see-also




<a href="https://msdn.microsoft.com/ed0e100e-9f82-48c0-b4bb-72820c5eeaa8">PdhSetQueryTimeRange</a>
 

 

