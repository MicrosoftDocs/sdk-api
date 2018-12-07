---
UID: NF:synchapi.TryEnterCriticalSection
title: TryEnterCriticalSection function
author: windows-sdk-content
description: Attempts to enter a critical section without blocking. If the call is successful, the calling thread takes ownership of the critical section.
old-location: base\tryentercriticalsection.htm
tech.root: sync
ms.assetid: 5225bda1-6e20-4f6b-9f9b-633c62acfdce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TryEnterCriticalSection, TryEnterCriticalSection function, _win32_tryentercriticalsection, base.tryentercriticalsection, synchapi/TryEnterCriticalSection, winbase/TryEnterCriticalSection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - TryEnterCriticalSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TryEnterCriticalSection function


## -description


Attempts to enter a critical section without blocking. If the call is successful, the calling thread takes ownership of the critical section.


## -parameters




### -param lpCriticalSection [in, out]

A pointer to the critical section object.


## -returns



If the critical section is successfully entered or the current thread already owns the critical section, the return value is nonzero.

If another thread already owns the critical section, the return value is zero.




## -remarks



The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must call the 
<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a> or 
<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a> function to initialize the object.

To enable mutually exclusive use of a shared resource, each thread calls the 
<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a> or 
<b>TryEnterCriticalSection</b> function to request ownership of the critical section before executing any section of code that uses the protected resource. The difference is that 
<b>TryEnterCriticalSection</b> returns immediately, regardless of whether it obtained ownership of the critical section, while 
<b>EnterCriticalSection</b> blocks until the thread can take ownership of the critical section. When it has finished executing the protected code, the thread uses the 
<a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a> function to relinquish ownership, enabling another thread to become the owner and gain access to the protected resource. The thread must call 
<b>LeaveCriticalSection</b> once for each time that it entered the critical section.

Any thread of the process can use the 
<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a> function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

If a thread terminates while it has ownership of a critical section, the state of the critical section is undefined.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a>



<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a>



<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>



<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a>



<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a>



<a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

