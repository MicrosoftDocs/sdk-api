---
UID: NF:threadpoolapiset.DisassociateCurrentThreadFromCallback
title: DisassociateCurrentThreadFromCallback function (threadpoolapiset.h)
description: Removes the association between the currently executing callback function and the object that initiated the callback. The current thread will no longer count as executing a callback on behalf of the object.
helpviewer_keywords: ["DisassociateCurrentThreadFromCallback","DisassociateCurrentThreadFromCallback function","base.disassociatecurrentthreadfromcallback","threadpoolapiset/DisassociateCurrentThreadFromCallback","winbase/DisassociateCurrentThreadFromCallback"]
old-location: base\disassociatecurrentthreadfromcallback.htm
tech.root: backup
ms.assetid: f25f936c-2570-4e8c-807b-42000cd878bb
ms.date: 12/05/2018
ms.keywords: DisassociateCurrentThreadFromCallback, DisassociateCurrentThreadFromCallback function, base.disassociatecurrentthreadfromcallback, threadpoolapiset/DisassociateCurrentThreadFromCallback, winbase/DisassociateCurrentThreadFromCallback
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
 - DisassociateCurrentThreadFromCallback
 - threadpoolapiset/DisassociateCurrentThreadFromCallback
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
 - DisassociateCurrentThreadFromCallback
---

# DisassociateCurrentThreadFromCallback function


## -description

Removes the association between the currently executing callback function and the object that initiated the callback.  The current thread will no longer count as executing a callback on behalf of the object.

## -parameters

### -param pci [in, out]

A pointer to a <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The pointer is passed to the callback function.

## -remarks

If this is the last thread executing a callback on behalf of the object, any threads waiting for the object's callbacks to complete will be released.

The thread remains associated with the object's <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">cleanup group</a> until the thread returns to the thread pool. This lets DLL shutdown routines safely synchronize with outstanding callbacks and proceed with unloading the DLL's code when all callbacks have completed.

The callback-generating object remains valid for the duration of the callback. The callback object may be reused or released (although synchronization with cleanup group release is still required).

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong">CallbackMayRunLong</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns">FreeLibraryWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns">ReleaseMutexWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns">SetEventWhenCallbackReturns</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback">TrySubmitThreadpoolCallback</a>