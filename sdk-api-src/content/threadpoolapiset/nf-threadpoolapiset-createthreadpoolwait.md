---
UID: NF:threadpoolapiset.CreateThreadpoolWait
title: CreateThreadpoolWait function
author: windows-sdk-content
description: Creates a new wait object.
old-location: base\createthreadpoolwait.htm
tech.root: procthread
ms.assetid: ba19f5f9-d4b0-4865-9609-95e7697d61c0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateThreadpoolWait, CreateThreadpoolWait function, base.createthreadpoolwait, threadpoolapiset/CreateThreadpoolWait, winbase/CreateThreadpoolWait
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - CreateThreadpoolWait
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateThreadpoolWait function


## -description


Creates a new wait object.


## -parameters




### -param pfnwa [in]

The callback function to call when the wait completes or times out. For details, see <a href="https://msdn.microsoft.com/96b924ba-b688-44f5-87a4-7a82a44e99ec">WaitCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_WAIT</b> structure that defines the wait object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To set the wait object, call the <a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a> function.

The work item and all functions it calls must be thread-pool safe. Therefore, you cannot call an asynchronous call that requires a persistent thread, such as the 
<a href="https://msdn.microsoft.com/aad72ed5-1123-4a8b-9fc4-b54a713b635e">RegNotifyChangeKeyValue</a> function, from the default callback environment. Instead, set the thread pool maximum equal to the thread pool minimum using the <a href="https://msdn.microsoft.com/381849cf-6835-40f2-be68-0522b16e4822">SetThreadpoolThreadMaximum</a> and <a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a> functions, or create your own thread using the <a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a> function.

<b>Windows 8:  </b><a href="https://msdn.microsoft.com/aad72ed5-1123-4a8b-9fc4-b54a713b635e">RegNotifyChangeKeyValue</a> can be called from a work item by setting the REG_NOTIFY_THREAD_AGNOSTIC flag.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f8323ad2-c0b6-4e5c-b6eb-7195673f8992">CloseThreadpoolWait</a>



<a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/49c40b35-a0ed-40a1-9c35-5d3985ebd98f">WaitForThreadpoolWaitCallbacks</a>
 

 

