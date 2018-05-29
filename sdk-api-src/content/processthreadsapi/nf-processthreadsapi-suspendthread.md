---
UID: NF:processthreadsapi.SuspendThread
title: SuspendThread function
author: windows-sdk-content
description: Suspends the specified thread.
old-location: base\suspendthread.htm
old-project: ProcThread
ms.assetid: 1332abcb-3356-4890-a03c-843358c1a3ce
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SuspendThread, SuspendThread function, _win32_suspendthread, base.suspendthread, processthreadsapi/SuspendThread, winbase/SuspendThread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
-	SuspendThread
product: Windows
targetos: Windows
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SuspendThread function


## -description


Suspends the specified thread.

A 64-bit application can suspend a WOW64 thread using the <a href="https://msdn.microsoft.com/d976675a-5400-41ac-a11d-c39a1b2dd50d">Wow64SuspendThread</a> function.


## -parameters




### -param hThread [in]

A handle to the thread that is to be suspended.

The handle must have the <b>THREAD_SUSPEND_RESUME</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is the thread's previous suspend count; otherwise, it is <code>(DWORD) -1</code>. To get extended error information, use the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



If the function succeeds, execution of the specified thread is suspended and the thread's suspend count is incremented. Suspending a thread causes the thread to stop executing user-mode (application) code.

This function is primarily designed for use by debuggers. It is not intended to be used for thread synchronization. Calling 
<b>SuspendThread</b> on a thread that owns a synchronization object, such as a mutex or critical section, can lead to a deadlock if the calling thread tries to obtain a synchronization object owned by a suspended thread. To avoid this situation, a thread within an application that is not a debugger should signal the other thread to suspend itself. The target thread must be designed to watch for this signal and respond appropriately.

Each thread has a suspend count (with a maximum value of <b>MAXIMUM_SUSPEND_COUNT</b>). If the suspend count is greater than zero, the thread is suspended; otherwise, the thread is not suspended and is eligible for execution. Calling 
<b>SuspendThread</b> causes the target thread's suspend count to be incremented. Attempting to increment past the maximum suspend count causes an error without incrementing the count.

The 
<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a> function decrements the suspend count of a suspended thread.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/ffc4e474-635b-4bf7-a68f-073899fb3fde">ResumeThread</a>



<a href="https://msdn.microsoft.com/b76d7af7-e3ec-4663-a9e7-832c01733c8c">Suspending Thread Execution</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

