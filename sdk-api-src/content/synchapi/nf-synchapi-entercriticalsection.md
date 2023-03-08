---
UID: NF:synchapi.EnterCriticalSection
title: EnterCriticalSection function (synchapi.h)
description: Waits for ownership of the specified critical section object. The function returns when the calling thread is granted ownership.
old-location: base\entercriticalsection.htm
tech.root: base
ms.assetid: bb307b7a-66fc-4d19-b774-deca8bf90492
ms.date: 12/05/2018
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

This function can raise <b>EXCEPTION_POSSIBLE_DEADLOCK</b>, also known as <b>STATUS_POSSIBLE_DEADLOCK</b>, if a wait operation on the critical section times out. The timeout interval is specified by the following registry value: <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager</b>&#92;<b>CriticalSectionTimeout</b>. Do not handle a possible deadlock exception; instead, debug the application.

## -remarks

The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a> to initialize the object.

To enable mutually exclusive access to a shared resource, each thread calls the 
<b>EnterCriticalSection</b> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-tryentercriticalsection">TryEnterCriticalSection</a> function to request ownership of the critical section before executing any section of code that accesses the protected resource. The difference is that 
<b>TryEnterCriticalSection</b> returns immediately, regardless of whether it obtained ownership of the critical section, while 
<b>EnterCriticalSection</b> blocks until the thread can take ownership of the critical section. When it has finished executing the protected code, the thread uses the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection">LeaveCriticalSection</a> function to relinquish ownership, enabling another thread to become owner and access the protected resource. There is no guarantee about the order in which waiting threads will acquire ownership of the critical section.

After a thread has ownership of a critical section, it can make additional calls to 
<b>EnterCriticalSection</b> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-tryentercriticalsection">TryEnterCriticalSection</a> without blocking its execution. This prevents a thread from deadlocking itself while waiting for a critical section that it already owns. The thread enters the critical section each time 
<b>EnterCriticalSection</b> and 
<b>TryEnterCriticalSection</b> succeed. A thread must call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection">LeaveCriticalSection</a> once for each time that it entered the critical section.

Any thread of the process can use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a> function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

If a thread terminates while it has ownership of a critical section, the state of the critical section is undefined.

If a critical section is deleted while it is still owned, the state of the threads waiting for ownership of the deleted critical section is undefined.

While a process is exiting, if a call to <b>EnterCriticalSection</b> would block, it will instead terminate the process immediately. This may cause global destructors to not be called.

#### Examples

For an example that uses 
<b>EnterCriticalSection</b>, see 
<a href="/windows/desktop/Sync/using-critical-section-objects">Using Critical Section Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/critical-section-objects">Critical Section Objects</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection">LeaveCriticalSection</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-tryentercriticalsection">TryEnterCriticalSection</a>
