---
UID: NF:threadpoollegacyapiset.UnregisterWaitEx
title: UnregisterWaitEx function (threadpoollegacyapiset.h)
description: Cancels a registered wait operation issued by the RegisterWaitForSingleObject function. (UnregisterWaitEx)
helpviewer_keywords: ["UnregisterWaitEx","UnregisterWaitEx function","_win32_unregisterwaitex","base.unregisterwaitex","threadpoollegacyapiset/UnregisterWaitEx","winbase/UnregisterWaitEx"]
old-location: base\unregisterwaitex.htm
tech.root: backup
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
ms.date: 12/05/2018
ms.keywords: UnregisterWaitEx, UnregisterWaitEx function, _win32_unregisterwaitex, base.unregisterwaitex, threadpoollegacyapiset/UnregisterWaitEx, winbase/UnregisterWaitEx
req.header: threadpoollegacyapiset.h
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
 - UnregisterWaitEx
 - threadpoollegacyapiset/UnregisterWaitEx
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
 - API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - UnregisterWaitEx
---

# UnregisterWaitEx function


## -description

Cancels a registered wait operation issued by the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function.

## -parameters

### -param WaitHandle [in]

The wait handle. This handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function.

### -param CompletionEvent [in, optional]

A handle to the event object to be signaled when the wait operation has been unregistered. This parameter can be <b>NULL</b>.

If this parameter is <b>INVALID_HANDLE_VALUE</b>, the function waits for all callback functions to complete before returning.

If this parameter is <b>NULL</b>, the function marks the timer for deletion and returns immediately. However, most callers should wait for the callback function to complete so they can perform any needed cleanup.

If the caller provides this event and the function succeeds or the function fails with  <b>ERROR_IO_PENDING</b>,  do not close the event until it is signaled.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You cannot make a blocking call to 
<b>UnregisterWaitEx</b> from within a callback function for the same wait operation. Otherwise, the callback will be waiting for itself to finish. In general, a blocking call to <b>UnregisterWaitEx</b> creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.

Be careful when making a blocking <b>UnregisterWaitEx</b> call on a persistent thread. If the wait operation being unregistered was created with   <b>WT_EXECUTEINPERSISTENTTHREAD</b>, a deadlock may occur.

After making non-blocking call to <b>UnregisterWaitEx</b>, no new callback functions associated with <i>WaitHandle</i> can be queued. However, there may be pending callback functions already queued to worker threads.

Under some conditions, the function will fail with <b>ERROR_IO_PENDING</b> if <i>CompletionEvent</i> is <b>NULL</b>. This indicates that there are outstanding callback functions. Those callbacks either will execute or are in the middle of executing.

If <i>CompletionEvent</i> is a handle to an event provided by the caller, it is possible for the function to succeed, fail with <b>ERROR_IO_PENDING</b>, or fail with a different error code. If the function succeeds, or if the function fails with <b>ERROR_IO_PENDING</b>, the caller should always wait until the event is signaled to close the event. If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.  

<b>Windows XP:  </b>If <i>CompletionEvent</i> is a handle to an event provided by the caller and the function fails with  <b>ERROR_IO_PENDING</b>,  the caller should wait until the event is signaled to close the event. This behavior changed starting with Windows Vista.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>
