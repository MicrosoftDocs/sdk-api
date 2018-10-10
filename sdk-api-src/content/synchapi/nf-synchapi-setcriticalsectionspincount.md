---
UID: NF:synchapi.SetCriticalSectionSpinCount
title: SetCriticalSectionSpinCount function
author: windows-sdk-content
description: Sets the spin count for the specified critical section.
old-location: base\setcriticalsectionspincount.htm
tech.root: Sync
ms.assetid: 4d435c70-2e9b-4923-8726-9c8143dceb15
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: SetCriticalSectionSpinCount, SetCriticalSectionSpinCount function, _win32_setcriticalsectionspincount, base.setcriticalsectionspincount, synchapi/SetCriticalSectionSpinCount, winbase/SetCriticalSectionSpinCount
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
 - SetCriticalSectionSpinCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCriticalSectionSpinCount function


## -description


Sets the spin count for the specified critical section. Spinning means that when a thread tries to acquire a critical section that is locked, the thread enters a loop, checks to see if the lock is released, and if the lock is not released, the thread goes to sleep.




## -parameters




### -param lpCriticalSection [in, out]

A pointer to the critical section object.


### -param dwSpinCount [in]

The spin count for the critical section object. On single-processor systems, the spin count is ignored and the critical section spin count is set to zero (0). On multiprocessor systems, if the critical section is unavailable, the calling thread spins <i>dwSpinCount</i> times before performing a wait operation on a semaphore associated with the critical section. If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.


## -returns



The function returns the previous spin count for the critical section.




## -remarks



The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must call the 
<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a> or 
<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a> function to initialize the object. You can subsequently modify the spin count by calling the 
<b>SetCriticalSectionSpinCount</b> function.

The spin count is useful for critical sections of short duration that can experience high levels of contention. Consider a worst-case scenario, in which an application on an SMP system has two or three threads constantly allocating and releasing memory from the heap. The application serializes the heap with a critical section. In the worst-case scenario, contention for the critical section is constant, and each thread makes an processing-intensive call to the 
<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a> function. However, if the spin count is set properly, the calling thread does not immediately call 
<b>WaitForSingleObject</b> when contention occurs. Instead, the calling thread can acquire ownership of the critical section if it is released during the spin operation.

You can improve performance significantly by choosing a small spin count for a critical section of short duration. The heap manager uses a spin count of roughly 4000 for its per-heap critical sections. This gives great performance and scalability in almost all worst-case scenarios.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0403 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a>



<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a>



<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>
 

 

