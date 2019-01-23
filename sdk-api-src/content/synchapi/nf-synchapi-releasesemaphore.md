---
UID: NF:synchapi.ReleaseSemaphore
title: ReleaseSemaphore function
author: windows-sdk-content
description: Increases the count of the specified semaphore object by a specified amount.
old-location: base\releasesemaphore.htm
tech.root: Sync
ms.assetid: 9d444318-4d66-4ec3-a65d-bd3b75db9d9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReleaseSemaphore, ReleaseSemaphore function, _win32_releasesemaphore, base.releasesemaphore, synchapi/ReleaseSemaphore, winbase/ReleaseSemaphore
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ReleaseSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReleaseSemaphore function


## -description


Increases the count of the specified semaphore object by a specified amount.


## -parameters




### -param hSemaphore [in]

A handle to the semaphore object. The 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> or 
<a href="https://msdn.microsoft.com/en-us/library/ms684326(v=VS.85).aspx">OpenSemaphore</a> function returns this handle.

This handle must have the <b>SEMAPHORE_MODIFY_STATE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param lReleaseCount [in]

The amount by which the semaphore object's current count is to be increased. The value must be greater than zero. If the specified amount would cause the semaphore's count to exceed the maximum count that was specified when the semaphore was created, the count is not changed and the function returns <b>FALSE</b>.


### -param lpPreviousCount [out, optional]

A pointer to a variable to receive the previous count for the semaphore. This parameter can be <b>NULL</b> if the previous count is not required.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The state of a semaphore object is signaled when its count is greater than zero and nonsignaled when its count is equal to zero. The process that calls the 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> function specifies the semaphore's initial count. Each time a waiting thread is released because of the semaphore's signaled state, the count of the semaphore is decreased by one.

Typically, an application uses a semaphore to limit the number of threads using a resource. Before a thread uses the resource, it specifies the semaphore handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. When the wait function returns, it decreases the semaphore's count by one. When the thread has finished using the resource, it calls 
<b>ReleaseSemaphore</b> to increase the semaphore's count by one.

Another use of 
<b>ReleaseSemaphore</b> is during an application's initialization. The application can create a semaphore with an initial count of zero. This sets the semaphore's state to nonsignaled and blocks all threads from accessing the protected resource. When the application finishes its initialization, it uses 
<b>ReleaseSemaphore</b> to increase the count to its maximum value, to permit normal access to the protected resource.

It is not possible to reduce the semaphore object count using 
<b>ReleaseSemaphore</b>, because <i>lReleaseCount</i> cannot be a negative number. To temporarily restrict or reduce access, create a loop in which you call the 
<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a> function with a time-out interval of zero until the semaphore count has been reduced sufficiently. (Note that other threads can reduce the count while this loop is being executed.) To restore access, call 
<b>ReleaseSemaphore</b> with the release count equal to the number of times 
<b>WaitForSingleObject</b> was called in the loop.


#### Examples

For an example that uses 
<b>ReleaseSemaphore</b>, see 
<a href="https://msdn.microsoft.com/24a5c13c-573a-4fc2-ac19-98188c9eb68a">Using Semaphore Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684326(v=VS.85).aspx">OpenSemaphore</a>



<a href="https://msdn.microsoft.com/d9da1d98-a306-4e2d-a149-1eef6a724751">Semaphore Objects</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

