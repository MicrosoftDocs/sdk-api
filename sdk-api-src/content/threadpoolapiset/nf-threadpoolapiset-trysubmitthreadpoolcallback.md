---
UID: NF:threadpoolapiset.TrySubmitThreadpoolCallback
title: TrySubmitThreadpoolCallback function (threadpoolapiset.h)
description: Requests that a thread pool worker thread call the specified callback function.
helpviewer_keywords: ["TrySubmitThreadpoolCallback","TrySubmitThreadpoolCallback function","base.trysubmitthreadpoolcallback","threadpoolapiset/TrySubmitThreadpoolCallback","winbase/TrySubmitThreadpoolCallback"]
old-location: base\trysubmitthreadpoolcallback.htm
tech.root: backup
ms.assetid: 689d197e-195f-419c-9317-b30c614038c4
ms.date: 12/05/2018
ms.keywords: TrySubmitThreadpoolCallback, TrySubmitThreadpoolCallback function, base.trysubmitthreadpoolcallback, threadpoolapiset/TrySubmitThreadpoolCallback, winbase/TrySubmitThreadpoolCallback
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - TrySubmitThreadpoolCallback
 - threadpoolapiset/TrySubmitThreadpoolCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - TrySubmitThreadpoolCallback
---

# TrySubmitThreadpoolCallback function


## -description

Requests that a thread pool worker thread call the specified callback function.

## -parameters

### -param pfns [in]

The callback function. For details, see <a href="/previous-versions/windows/desktop/legacy/ms686295(v=vs.85)">SimpleCallback</a>.

### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.

### -param pcbe [in, optional]

A pointer to a <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback function. Use the <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function to initialize the structure before calling this function.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.

## -returns

If the function succeeds, it returns TRUE.

If the function fails, it returns FALSE. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong">CallbackMayRunLong</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback">DisassociateCurrentThreadFromCallback</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns">ReleaseMutexWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns">SetEventWhenCallbackReturns</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>