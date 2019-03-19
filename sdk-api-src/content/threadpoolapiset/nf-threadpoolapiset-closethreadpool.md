---
UID: NF:threadpoolapiset.CloseThreadpool
title: CloseThreadpool function (threadpoolapiset.h)
author: windows-sdk-content
description: Closes the specified thread pool.
old-location: base\closethreadpool.htm
tech.root: ProcThread
ms.assetid: 84f673b5-d9b1-4f3d-9ae6-b1ad173268cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseThreadpool, CloseThreadpool function, base.closethreadpool, threadpoolapiset/CloseThreadpool, winbase/CloseThreadpool
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
 - CloseThreadpool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseThreadpool function


## -description


Closes the specified thread pool.


## -parameters




### -param ptpp [in, out]

A <b>TP_POOL</b> structure that defines the thread pool. The <a href="https://msdn.microsoft.com/cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6">CreateThreadpool</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The thread pool is closed immediately if there are no outstanding <a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">work</a>, <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">I/O</a>, <a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">timer</a>, or <a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">wait</a> objects that are bound to the pool; otherwise, the thread pool is released asynchronously after the outstanding objects are freed.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6">CreateThreadpool</a>



<a href="https://msdn.microsoft.com/381849cf-6835-40f2-be68-0522b16e4822">SetThreadpoolThreadMaximum</a>



<a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

