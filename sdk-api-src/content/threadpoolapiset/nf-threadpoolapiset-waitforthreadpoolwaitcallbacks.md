---
UID: NF:threadpoolapiset.WaitForThreadpoolWaitCallbacks
title: WaitForThreadpoolWaitCallbacks function (threadpoolapiset.h)
description: Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
helpviewer_keywords: ["WaitForThreadpoolWaitCallbacks","WaitForThreadpoolWaitCallbacks function","base.waitforthreadpoolwaitcallbacks","threadpoolapiset/WaitForThreadpoolWaitCallbacks","winbase/WaitForThreadpoolWaitCallbacks"]
old-location: base\waitforthreadpoolwaitcallbacks.htm
tech.root: backup
ms.assetid: 49c40b35-a0ed-40a1-9c35-5d3985ebd98f
ms.date: 12/05/2018
ms.keywords: WaitForThreadpoolWaitCallbacks, WaitForThreadpoolWaitCallbacks function, base.waitforthreadpoolwaitcallbacks, threadpoolapiset/WaitForThreadpoolWaitCallbacks, winbase/WaitForThreadpoolWaitCallbacks
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
 - WaitForThreadpoolWaitCallbacks
 - threadpoolapiset/WaitForThreadpoolWaitCallbacks
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
 - WaitForThreadpoolWaitCallbacks
---

# WaitForThreadpoolWaitCallbacks function


## -description

Waits for outstanding wait callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.

## -parameters

### -param pwa [in, out]

A pointer to a <b>TP_WAIT</b> structure that defines the wait object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a> function returns this pointer.

### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait">CloseThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait">CreateThreadpoolWait</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>