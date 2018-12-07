---
UID: NF:threadpoolapiset.SetThreadpoolThreadMaximum
title: SetThreadpoolThreadMaximum function
author: windows-sdk-content
description: Sets the maximum number of threads that the specified thread pool can allocate to process callbacks.
old-location: base\setthreadpoolthreadmaximum.htm
tech.root: procthread
ms.assetid: 381849cf-6835-40f2-be68-0522b16e4822
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetThreadpoolThreadMaximum, SetThreadpoolThreadMaximum function, base.setthreadpoolthreadmaximum, threadpoolapiset/SetThreadpoolThreadMaximum
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
 - SetThreadpoolThreadMaximum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadpoolThreadMaximum function


## -description


Sets the maximum number of threads that the specified thread pool can allocate to process callbacks.


## -parameters




### -param ptpp [in, out]

A <b>TP_POOL</b> structure that defines the thread pool. The <a href="https://msdn.microsoft.com/cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6">CreateThreadpool</a> function returns this structure.


### -param cthrdMost [in]

The maximum number of threads.


## -returns



This function does not return a value.




## -remarks



To specify the minimum number of threads available in the pool, call <a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/84f673b5-d9b1-4f3d-9ae6-b1ad173268cd">CloseThreadpool</a>



<a href="https://msdn.microsoft.com/cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6">CreateThreadpool</a>



<a href="https://msdn.microsoft.com/39ab262d-50ff-4aaa-93a8-ded2b0f72615">SetThreadpoolThreadMinimum</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

