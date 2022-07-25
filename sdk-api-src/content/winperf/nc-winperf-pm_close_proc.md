---
UID: NC:winperf.PM_CLOSE_PROC
title: PM_CLOSE_PROC (winperf.h)
description: Performs the cleanup required by your performance DLL.
helpviewer_keywords: ["ClosePerformanceData","ClosePerformanceData callback function [Perf]","PM_CLOSE_PROC","PM_CLOSE_PROC callback","base.closeperformancedata","perf.closeperformancedata","winperf/ClosePerformanceData"]
old-location: perf\closeperformancedata.htm
tech.root: perf
ms.assetid: fb97f68d-4992-4969-9b6b-ace26dcd3155
ms.date: 12/05/2018
ms.keywords: ClosePerformanceData, ClosePerformanceData callback function [Perf], PM_CLOSE_PROC, PM_CLOSE_PROC callback, base.closeperformancedata, perf.closeperformancedata, winperf/ClosePerformanceData
req.header: winperf.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PM_CLOSE_PROC
 - winperf/PM_CLOSE_PROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winperf.h
api_name:
 - ClosePerformanceData
---

# PM_CLOSE_PROC callback function


## -description

Performs the cleanup required by your performance DLL. Implement and export this function if you are writing a performance DLL to provide performance data. The system calls this function whenever a consumer closes the registry key used to collect performance data.

The <b>ClosePerformanceData</b> function is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

## -returns

This function should return ERROR_SUCCESS.

## -see-also

<a href="/windows/desktop/api/winperf/nc-winperf-pm_collect_proc">CollectPerformanceData</a>



<a href="/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)">OpenPerformanceData</a>