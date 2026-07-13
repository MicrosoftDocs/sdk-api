---
UID: NF:synchapi.EnterCriticalSection
title: EnterCriticalSection function (synchapi.h)
description: Waits for ownership of the specified critical section object. The function returns when the calling thread is granted ownership.
old-location: base\entercriticalsection.htm
tech.root: base
ms.assetid: bb307b7a-66fc-4d19-b774-deca8bf90492
ms.date: 02/05/2024
ms.keywords: EnterCriticalSection, EnterCriticalSection function, _win32_entercriticalsection, base.entercriticalsection, synchapi/EnterCriticalSection, winbase/EnterCriticalSection
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
 - EnterCriticalSection
 - synchapi/EnterCriticalSection
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
 - EnterCriticalSection
---

# EnterCriticalSection function

## -description

Waits for ownership of the specified critical section object. The function returns when the calling thread is granted ownership.

## -parameters

### -param lpCriticalSection [in, out]

A pointer to the critical section object.

## -returns

This function does not return a value.

This function can raise **EXCEPTION_POSSIBLE_DEADLOCK**, also known as **STATUS_POSSIBLE_DEADLOCK**, if a wait operation on the critical section times out. The timeout interval is specified by the following registry value: **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager**&#92;**CriticalSectionTimeout**. Do not handle a possible deadlock exception; instead, debug the application.

## -remarks

The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must call [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) or [InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md) to initialize the object.

To enable mutually exclusive access to a shared resource, each thread calls the **EnterCriticalSection** or [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md) function to request ownership of the critical section before executing any section of code that accesses the protected resource. The difference is that **TryEnterCriticalSection** returns immediately, regardless of whether it obtained ownership of the critical section, while **EnterCriticalSection** blocks until the thread can take ownership of the critical section. When it has finished executing the protected code, the thread uses the [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md) function to relinquish ownership, enabling another thread to become owner and access the protected resource. There is no guarantee about the order in which waiting threads will acquire ownership of the critical section.

After a thread has ownership of a critical section, it can make additional calls to **EnterCriticalSection** or [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md) without blocking its execution. This prevents a thread from deadlocking itself while waiting for a critical section that it already owns. The thread enters the critical section each time **EnterCriticalSection** and **TryEnterCriticalSection** succeed. A thread must call [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md) once for each time that it entered the critical section.

Any thread of the process can use the [DeleteCriticalSection](nf-synchapi-deletecriticalsection.md) function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

If a thread terminates while it has ownership of a critical section, the state of the critical section is undefined.

If a critical section is deleted while it is still owned, the state of the threads waiting for ownership of the deleted critical section is undefined.

While a process is exiting, if a call to **EnterCriticalSection** would block, it will instead terminate the process immediately. This may cause global destructors to not be called.

#### Examples

For an example that uses **EnterCriticalSection**, see [Using Critical Section Objects](/windows/win32/Sync/using-critical-section-objects).

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[DeleteCriticalSection](nf-synchapi-deletecriticalsection.md)

[InitializeCriticalSection](nf-synchapi-initializecriticalsection.md)

[InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md)

[LeaveCriticalSection](nf-synchapi-leavecriticalsection.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
