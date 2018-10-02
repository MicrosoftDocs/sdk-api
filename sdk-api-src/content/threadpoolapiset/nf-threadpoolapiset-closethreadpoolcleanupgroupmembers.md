---
UID: NF:threadpoolapiset.CloseThreadpoolCleanupGroupMembers
title: CloseThreadpoolCleanupGroupMembers function
author: windows-sdk-content
description: Releases the members of the specified cleanup group, waits for all callback functions to complete, and optionally cancels any outstanding callback functions.
old-location: base\closethreadpoolcleanupgroupmembers.htm
tech.root: ProcThread
ms.assetid: 9c78db13-d8dd-4eda-83d9-c9dbbfc6e822
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CloseThreadpoolCleanupGroupMembers, CloseThreadpoolCleanupGroupMembers function, base.closethreadpoolcleanupgroupmembers, threadpoolapiset/CloseThreadpoolCleanupGroupMembers, winbase/CloseThreadpoolCleanupGroupMembers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseThreadpoolCleanupGroupMembers function


## -description


Releases the members of the specified cleanup group, waits for all callback functions to complete, and optionally cancels any outstanding callback functions.


## -parameters




### -param ptpcg [in, out]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a> function returns this structure.


### -param fCancelPendingCallbacks [in]

If this parameter is TRUE, the function cancels outstanding callbacks that have not yet started. If this parameter is FALSE, the function waits for outstanding callback functions to complete.


### -param pvCleanupContext [in, out, optional]

The application-defined data to pass to the application's cleanup group callback function. You can specify the callback function when you call <a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>.


## -returns



This function does not return a value.




## -remarks



The <b>CloseThreadpoolCleanupGroupMembers</b> function simplifies cleanup of thread pool callback objects by releasing, in a single operation, all work objects, wait objects, and timer objects that are members of the cleanup group. An object becomes a member of a cleanup group when the object is created with the threadpool callback environment that was specified when the cleanup group was created. For more information, see <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a>.

The <b>CloseThreadpoolCleanupGroupMembers</b> function blocks until all currently executing callback functions finish. If <i>fCancelPendingCallbacks</i> is TRUE, outstanding callbacks are canceled; otherwise, the function blocks until all outstanding callbacks also finish.  After the <b>CloseThreadpoolCleanupGroupMembers</b> function returns, an application should not use any object that was a member of the cleanup group at the time <b>CloseThreadpoolCleanupGroupMembers</b> was called.  Also, an application should not release any of the objects individually by calling a function such as <a href="https://msdn.microsoft.com/89d7362e-0814-4f7e-a27f-8a297e210559">CloseThreadpoolWork</a>, because the objects have already been released. 

The <b>CloseThreadpoolCleanupGroupMembers</b> function does not close the cleanup group itself. Instead, the cleanup group persists until the <a href="https://msdn.microsoft.com/e38e4d99-63f2-4bac-8675-cf0f3aa149a7">CloseThreadpoolCleanupGroup</a> function is called. Also, closing a cleanup group does not affect the associated threadpool callback environment. The callback environment persists until it is destroyed by calling <a href="https://msdn.microsoft.com/b6a635f3-a603-4c2f-9aa9-1baa51922394">DestroyThreadpoolEnvironment</a>.

 As long as a cleanup group persists, new objects created with the cleanup group's associated threadpool callback environment are added to the cleanup group. This allows an application to reuse the cleanup group. However, it can lead to errors if the application does not synchronize code that calls <b>CloseThreadpoolCleanupGroupMembers</b> with code that creates new objects. For example, suppose a thread creates two threadpool work objects, Work1 and Work2. Another thread calls <b>CloseThreadpoolCleanupGroupMembers</b>. Depending on when the threads run, any of the following might occur: 

<ul>
<li>Work1 and Work2 are added to the cleanup group after its existing members were released. Code that submits Work1 and Work2 will succeed.</li>
<li>Work1 is added to the cleanup group before its existing members are released, causing Work1 to be released along with other members. Then Work2 is added. Code that submits Work1 will generate an exception; code that submits Work2 will succeed.</li>
<li>Work1 and Work2 are added to the cleanup group before its existing members are released, causing both Work1 and Work2 to be released. Code that submits Work1 or Work2 will generate an exception.</li>
</ul>
To simply wait for or cancel pending work items without releasing them, use one of the threadpool callback functions: <a href="https://msdn.microsoft.com/68dc640d-8678-441d-88bd-01284d98a251">WaitForThreadpoolIoCallbacks</a>, <a href="https://msdn.microsoft.com/511488b8-9e92-47b9-8b3c-7ece9d9f996c">WaitForThreadpoolTimerCallbacks</a>, <a href="https://msdn.microsoft.com/49c40b35-a0ed-40a1-9c35-5d3985ebd98f">WaitForThreadpoolWaitCallbacks</a>, or <a href="https://msdn.microsoft.com/97c16892-d6ef-4216-ac79-344e83ab35bc">WaitForThreadpoolWorkCallbacks</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e38e4d99-63f2-4bac-8675-cf0f3aa149a7">CloseThreadpoolCleanupGroup</a>



<a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

