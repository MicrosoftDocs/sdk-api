---
UID: NF:winbase.GetProcessIoCounters
title: GetProcessIoCounters function (winbase.h)
description: Retrieves accounting information for all I/O operations performed by the specified process.
helpviewer_keywords: ["GetProcessIoCounters","GetProcessIoCounters function","_win32_getprocessiocounters","base.getprocessiocounters","winbase/GetProcessIoCounters"]
old-location: base\getprocessiocounters.htm
tech.root: backup
ms.assetid: e6973c1b-86bc-4fd1-aff6-26e87f8013c4
ms.date: 12/05/2018
ms.keywords: GetProcessIoCounters, GetProcessIoCounters function, _win32_getprocessiocounters, base.getprocessiocounters, winbase/GetProcessIoCounters
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessIoCounters
 - winbase/GetProcessIoCounters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-processtopology-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
api_name:
 - GetProcessIoCounters
---

# GetProcessIoCounters function


## -description

Retrieves accounting information for all I/O operations performed by the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

### -param lpIoCounters [out]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-io_counters">IO_COUNTERS</a> structure that receives the I/O accounting information for the process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-io_counters">IO_COUNTERS</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>