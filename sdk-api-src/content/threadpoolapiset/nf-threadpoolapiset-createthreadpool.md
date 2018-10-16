---
UID: NF:threadpoolapiset.CreateThreadpool
title: CreateThreadpool function
author: windows-sdk-content
description: Allocates a new pool of threads to execute callbacks.
old-location: base\createthreadpool.htm
tech.root: procthread
ms.assetid: cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateThreadpool, CreateThreadpool function, base.createthreadpool, threadpoolapiset/CreateThreadpool, winbase/CreateThreadpool
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
 - CreateThreadpool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateThreadpool function


## -description


Allocates a new pool of threads to execute callbacks.


## -parameters




### -param reserved

This parameter is reserved and must be NULL.


## -returns



If the function succeeds, it returns a <b>TP_POOL</b> structure representing the newly allocated thread pool. Applications do not modify the members of this structure.

If function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After creating the new thread pool, you should call <a href="https://msdn.microsoft.com/381849cf-6835-40f2-be68-0522b16e4822">SetThreadpoolThreadMaximum</a> to specify the maximum number of threads that the pool can allocate and <a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a> to specify the minimum number of threads available in the pool.

To use the pool, you must associate the pool with a callback environment. To create the callback environment, call <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>. Then, call <a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a> to associate the pool with the callback environment.

To release the thread pool, call <a href="https://msdn.microsoft.com/84f673b5-d9b1-4f3d-9ae6-b1ad173268cd">CloseThreadpool</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/84f673b5-d9b1-4f3d-9ae6-b1ad173268cd">CloseThreadpool</a>



<a href="https://msdn.microsoft.com/381849cf-6835-40f2-be68-0522b16e4822">SetThreadpoolThreadMaximum</a>



<a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

