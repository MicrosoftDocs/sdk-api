---
UID: NF:threadpoolapiset.CloseThreadpoolCleanupGroupMembers
title: CloseThreadpoolCleanupGroupMembers function (threadpoolapiset.h)
description: Releases the members of the specified cleanup group, waits for all callback functions to complete, and optionally cancels any outstanding callback functions.
helpviewer_keywords: ["CloseThreadpoolCleanupGroupMembers","CloseThreadpoolCleanupGroupMembers function","base.closethreadpoolcleanupgroupmembers","threadpoolapiset/CloseThreadpoolCleanupGroupMembers","winbase/CloseThreadpoolCleanupGroupMembers"]
old-location: base\closethreadpoolcleanupgroupmembers.htm
tech.root: backup
ms.assetid: 9c78db13-d8dd-4eda-83d9-c9dbbfc6e822
ms.date: 12/05/2018
ms.keywords: CloseThreadpoolCleanupGroupMembers, CloseThreadpoolCleanupGroupMembers function, base.closethreadpoolcleanupgroupmembers, threadpoolapiset/CloseThreadpoolCleanupGroupMembers, winbase/CloseThreadpoolCleanupGroupMembers
req.header: threadpoolapiset.h
req.include-header: Windows.h
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
 - CloseThreadpoolCleanupGroupMembers
 - threadpoolapiset/CloseThreadpoolCleanupGroupMembers
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
 - CloseThreadpoolCleanupGroupMembers
---

# CloseThreadpoolCleanupGroupMembers function


## -description

Releases the members of the specified cleanup group, waits for all callback functions to complete, and optionally cancels any outstanding callback functions.

## -parameters

### -param ptpcg [in, out]

A pointer to a <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a> function returns this pointer.

### -param fCancelPendingCallbacks [in]

If this parameter is TRUE, the function cancels outstanding callbacks that have not yet started. If this parameter is FALSE, the function waits for outstanding callback functions to complete.

### -param pvCleanupContext [in, out, optional]

The application-defined data to pass to the application's cleanup group callback function. You can specify the callback function when you call <a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>.

## -remarks

The <b>CloseThreadpoolCleanupGroupMembers</b> function simplifies cleanup of thread pool callback objects by releasing, in a single operation, all work objects, wait objects, and timer objects that are members of the cleanup group. An object becomes a member of a cleanup group when the object is created with the threadpool callback environment that was specified when the cleanup group was created. For more information, see <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a>.

The <b>CloseThreadpoolCleanupGroupMembers</b> function blocks until all currently executing callback functions finish. If <i>fCancelPendingCallbacks</i> is TRUE, outstanding callbacks are canceled; otherwise, the function blocks until all outstanding callbacks also finish.  After the <b>CloseThreadpoolCleanupGroupMembers</b> function returns, an application should not use any object that was a member of the cleanup group at the time <b>CloseThreadpoolCleanupGroupMembers</b> was called.  Also, an application should not release any of the objects individually by calling a function such as <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork">CloseThreadpoolWork</a>, because the objects have already been released. 

The <b>CloseThreadpoolCleanupGroupMembers</b> function does not close the cleanup group itself. Instead, the cleanup group persists until the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup">CloseThreadpoolCleanupGroup</a> function is called. Also, closing a cleanup group does not affect the associated threadpool callback environment. The callback environment persists until it is destroyed by calling <a href="/windows/desktop/api/winbase/nf-winbase-destroythreadpoolenvironment">DestroyThreadpoolEnvironment</a>.

 As long as a cleanup group persists, new objects created with the cleanup group's associated threadpool callback environment are added to the cleanup group. This allows an application to reuse the cleanup group. However, it can lead to errors if the application does not synchronize code that calls <b>CloseThreadpoolCleanupGroupMembers</b> with code that creates new objects. For example, suppose a thread creates two threadpool work objects, Work1 and Work2. Another thread calls <b>CloseThreadpoolCleanupGroupMembers</b>. Depending on when the threads run, any of the following might occur: 

<ul>
<li>Work1 and Work2 are added to the cleanup group after its existing members were released. Code that submits Work1 and Work2 will succeed.</li>
<li>Work1 is added to the cleanup group before its existing members are released, causing Work1 to be released along with other members. Then Work2 is added. Code that submits Work1 will generate an exception; code that submits Work2 will succeed.</li>
<li>Work1 and Work2 are added to the cleanup group before its existing members are released, causing both Work1 and Work2 to be released. Code that submits Work1 or Work2 will generate an exception.</li>
</ul>
To simply wait for or cancel pending work items without releasing them, use one of the threadpool callback functions: <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks">WaitForThreadpoolIoCallbacks</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks">WaitForThreadpoolTimerCallbacks</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks">WaitForThreadpoolWaitCallbacks</a>, or <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks">WaitForThreadpoolWorkCallbacks</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-the-thread-pool-functions">Using the Thread Pool Functions</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup">CloseThreadpoolCleanupGroup</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackcleanupgroup">SetThreadpoolCallbackCleanupGroup</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>