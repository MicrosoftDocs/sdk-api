---
UID: NF:processthreadsapi.GetThreadIOPendingFlag
title: GetThreadIOPendingFlag function (processthreadsapi.h)
description: Determines whether a specified thread has any I/O requests pending.
helpviewer_keywords: ["GetThreadIOPendingFlag","GetThreadIOPendingFlag function","base.getthreadiopendingflag","processthreadsapi/GetThreadIOPendingFlag"]
old-location: base\getthreadiopendingflag.htm
tech.root: processthreadsapi
ms.assetid: 5502f735-38f5-44a4-908d-1b421ee66aec
ms.date: 12/05/2018
ms.keywords: GetThreadIOPendingFlag, GetThreadIOPendingFlag function, base.getthreadiopendingflag, processthreadsapi/GetThreadIOPendingFlag
req.header: processthreadsapi.h
req.include-header: Windows.h
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
 - GetThreadIOPendingFlag
 - processthreadsapi/GetThreadIOPendingFlag
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
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadIOPendingFlag
---

# GetThreadIOPendingFlag function


## -description

Determines whether a specified thread has any I/O requests pending.

## -parameters

### -param hThread [in]

A handle to the thread in question. This handle must have been created with the THREAD_QUERY_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param lpIOIsPending [in, out]

A pointer to a  variable which the function sets to TRUE if the specified thread has one or more I/O requests pending, or to FALSE otherwise.

## -returns

If the  function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Keep in mind that the I/O status of the specified thread can change  rapidly, and may already have changed by the time the function returns. For example, a pending I/O operation could complete between the time the function sets  <i>lpIOIsPending</i> and the time it returns.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>