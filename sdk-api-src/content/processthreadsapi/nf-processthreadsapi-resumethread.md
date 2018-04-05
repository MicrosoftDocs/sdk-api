---
UID: NF:processthreadsapi.ResumeThread
title: ResumeThread function
author: windows-driver-content
description: Decrements a thread's suspend count. When the suspend count is decremented to zero, the execution of the thread is resumed.
old-location: base\resumethread.htm
old-project: ProcThread
ms.assetid: ffc4e474-635b-4bf7-a68f-073899fb3fde
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ResumeThread, ResumeThread function, _win32_resumethread, base.resumethread, processthreadsapi/ResumeThread, winbase/ResumeThread
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	KernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-1.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l1-1-0.dll
-	API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
-	ResumeThread
product: Windows
targetos: Windows
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ResumeThread function


## -description


Decrements a thread's suspend count. When the suspend count is decremented to zero, the execution of the thread is resumed.


## -parameters




### -param hThread [in]

A handle to the thread to be restarted. 




This handle must have the THREAD_SUSPEND_RESUME access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is the thread's previous suspend count.

If the function fails, the return value is (DWORD) -1. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ResumeThread</b> function checks the suspend count of the subject thread. If the suspend count is zero, the thread is not currently suspended. Otherwise, the subject thread's suspend count is decremented. If the resulting value is zero, then the execution of the subject thread is resumed.

If the return value is zero, the specified thread was not suspended. If the return value is 1, the specified thread was suspended but was restarted. If the return value is greater than 1, the specified thread is still suspended.

Note that while reporting debug events, all threads within the reporting process are frozen. Debuggers are expected to use the 
<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a> and 
<b>ResumeThread</b> functions to limit the set of threads that can execute within a process. By suspending all threads in a process except for the one reporting a debug event, it is possible to "single step" a single thread. The other threads are not released by a continue operation if they are suspended.

<b>Windows Phone 8.1:  </b>This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.  





## -see-also




<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>



<a href="https://msdn.microsoft.com/b76d7af7-e3ec-4663-a9e7-832c01733c8c">Suspending Thread Execution</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

