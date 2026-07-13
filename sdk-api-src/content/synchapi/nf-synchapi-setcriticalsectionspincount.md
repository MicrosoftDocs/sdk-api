---
UID: NF:synchapi.SetCriticalSectionSpinCount
title: SetCriticalSectionSpinCount function (synchapi.h)
description: Sets the spin count for the specified critical section.
helpviewer_keywords: ["SetCriticalSectionSpinCount","SetCriticalSectionSpinCount function","_win32_setcriticalsectionspincount","base.setcriticalsectionspincount","synchapi/SetCriticalSectionSpinCount","winbase/SetCriticalSectionSpinCount"]
old-location: base\setcriticalsectionspincount.htm
tech.root: base
ms.assetid: 4d435c70-2e9b-4923-8726-9c8143dceb15
ms.date: 02/05/2024
ms.keywords: SetCriticalSectionSpinCount, SetCriticalSectionSpinCount function, _win32_setcriticalsectionspincount, base.setcriticalsectionspincount, synchapi/SetCriticalSectionSpinCount, winbase/SetCriticalSectionSpinCount
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetCriticalSectionSpinCount
 - synchapi/SetCriticalSectionSpinCount
dev_langs:
 - c++
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
 - vertdll.dll
api_name:
 - SetCriticalSectionSpinCount
---

# SetCriticalSectionSpinCount function

## -description

Sets the spin count for the specified critical section. Spinning means that when a thread tries to acquire a critical section that is locked, the thread enters a loop, checks to see if the lock is released, and if the lock is not released, the thread goes to sleep.

## -parameters

### -param lpCriticalSection [in, out]

A pointer to the critical section object.

### -param dwSpinCount [in]

The spin count for the critical section object. On single-processor systems, the spin count is ignored and the critical section spin count is set to zero (0). On multiprocessor systems, if the critical section is unavailable, the calling thread spins *dwSpinCount* times before performing a wait operation on a semaphore associated with the critical section. If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.

## -returns

The function returns the previous spin count for the critical section.

## -remarks

The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must call the [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) or [InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md) function to initialize the object. You can subsequently modify the spin count by calling the **SetCriticalSectionSpinCount** function.

The spin count is useful for critical sections of short duration that can experience high levels of contention. Consider a worst-case scenario, in which an application on an SMP system has two or three threads constantly allocating and releasing memory from the heap. The application serializes the heap with a critical section. In the worst-case scenario, contention for the critical section is constant, and each thread makes a processing-intensive call to the [WaitForSingleObject](nf-synchapi-waitforsingleobject.md) function. However, if the spin count is set properly, the calling thread does not immediately call **WaitForSingleObject** when contention occurs. Instead, the calling thread can acquire ownership of the critical section if it is released during the spin operation.

You can improve performance significantly by choosing a small spin count for a critical section of short duration. The heap manager uses a spin count of roughly 4000 for its per-heap critical sections. This gives great performance and scalability in almost all worst-case scenarios.

To compile an application that uses this function, define **_WIN32_WINNT** as `0x0403` or later. For more information, see [Using the Windows Headers](/windows/win32/WinProg/using-the-windows-headers).

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[InitializeCriticalSection](nf-synchapi-initializecriticalsection.md)

[InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md)

[WaitForSingleObject](nf-synchapi-waitforsingleobject.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
