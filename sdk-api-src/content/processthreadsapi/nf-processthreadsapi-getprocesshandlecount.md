---
UID: NF:processthreadsapi.GetProcessHandleCount
title: GetProcessHandleCount function (processthreadsapi.h)
description: Retrieves the number of open handles that belong to the specified process.
helpviewer_keywords: ["GetProcessHandleCount","GetProcessHandleCount function","base.getprocesshandlecount","processthreadsapi/GetProcessHandleCount","winbase/GetProcessHandleCount"]
old-location: base\getprocesshandlecount.htm
tech.root: processthreadsapi
ms.assetid: bb8cf86b-00b8-4a64-90f8-66ac6dbf9dee
ms.date: 12/05/2018
ms.keywords: GetProcessHandleCount, GetProcessHandleCount function, base.getprocesshandlecount, processthreadsapi/GetProcessHandleCount, winbase/GetProcessHandleCount
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
 - GetProcessHandleCount
 - processthreadsapi/GetProcessHandleCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetProcessHandleCount
---

# GetProcessHandleCount function


## -description

Retrieves the number of open handles  that belong to the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose handle count is being requested.  The
        handle must have the PROCESS_QUERY_INFORMATION
        or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.

### -param pdwHandleCount [in, out]

A pointer to a variable that receives the number of open handles that belong to the specified process.

## -returns

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error  information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function retrieves information about the executive objects for the process. For more information, see <a href="/windows/desktop/SysInfo/kernel-objects">Kernel Objects</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>