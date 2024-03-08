---
UID: NF:synchapi.InitializeCriticalSectionEx
title: InitializeCriticalSectionEx function (synchapi.h)
description: Initializes a critical section object with a spin count and optional flags.
helpviewer_keywords: ["CRITICAL_SECTION_NO_DEBUG_INFO","InitializeCriticalSectionEx","InitializeCriticalSectionEx function","base.initializecriticalsectionex","synchapi/InitializeCriticalSectionEx","winbase/InitializeCriticalSectionEx"]
old-location: base\initializecriticalsectionex.htm
tech.root: base
ms.assetid: da84b187-0eb7-4363-8e68-8a525586d7d9
ms.date: 02/05/2024
ms.keywords: CRITICAL_SECTION_NO_DEBUG_INFO, InitializeCriticalSectionEx, InitializeCriticalSectionEx function, base.initializecriticalsectionex, synchapi/InitializeCriticalSectionEx, winbase/InitializeCriticalSectionEx
req.header: synchapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeCriticalSectionEx
 - synchapi/InitializeCriticalSectionEx
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
 - InitializeCriticalSectionEx
---

# InitializeCriticalSectionEx function

## -description

Initializes a critical section object with a spin count and optional flags.

## -parameters

### -param lpCriticalSection [out]

A pointer to the critical section object.

### -param dwSpinCount [in]

The spin count for the critical section object. On single-processor systems, the spin count is ignored and the critical section spin count is set to 0 (zero). On multiprocessor systems, if the critical section is unavailable, the calling thread spin *dwSpinCount* times before performing a wait operation on a semaphore associated with the critical section. If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.

### -param Flags [in]

This parameter can be 0 or the following value.

| Value | Meaning |
|-------|---------|
| **CRITICAL_SECTION_NO_DEBUG_INFO** | The critical section is created without debug information. |

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

The threads of a single process can use a critical section object for mutual-exclusion synchronization. There is no guarantee about the order that threads obtain ownership of the critical section, however, the system is fair to all threads.

The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must initialize the object. You can subsequently modify the spin count by calling the [SetCriticalSectionSpinCount](nf-synchapi-setcriticalsectionspincount.md) function.

After a critical section object is initialized, the threads of the process can specify the object in the [EnterCriticalSection](nf-synchapi-entercriticalsection.md), [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md), or [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md) function to provide mutually exclusive access to a shared resource. For similar synchronization between the threads of different processes, use a mutex object.

A critical section object cannot be moved or copied. The process must also not modify the object, but must treat it as logically opaque. Use only the critical section functions to manage critical section objects. When you have finished using the critical section, call the [DeleteCriticalSection](nf-synchapi-deletecriticalsection.md) function.

A critical section object must be deleted before it can be reinitialized. Initializing a critical section that is already  initialized results in undefined behavior.

The spin count is useful for critical sections of short duration that can experience high levels of contention. Consider a worst-case scenario, in which an application on an SMP system has two or three threads constantly allocating and releasing memory from the heap. The application serializes the heap with a critical section. In the worst-case scenario, contention for the critical section is constant, and each thread makes a processing-intensive call to the 
[WaitForSingleObject](nf-synchapi-waitforsingleobject.md) function. However, if the spin count is set properly, the calling thread does not immediately call **WaitForSingleObject** when contention occurs. Instead, the calling thread can acquire ownership of the critical section if it is released during the spin operation.

You can improve performance significantly by choosing a small spin count for a critical section of short duration. The heap manager uses a spin count of roughly 4000 for its per-heap critical sections. This gives great performance and scalability in almost all worst-case scenarios.

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[DeleteCriticalSection](nf-synchapi-deletecriticalsection.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
