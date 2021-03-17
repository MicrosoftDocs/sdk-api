---
UID: NF:synchapi.TryEnterCriticalSection
title: TryEnterCriticalSection function (synchapi.h)
description: Attempts to enter a critical section without blocking. If the call is successful, the calling thread takes ownership of the critical section.
helpviewer_keywords: ["TryEnterCriticalSection","TryEnterCriticalSection function","_win32_tryentercriticalsection","base.tryentercriticalsection","synchapi/TryEnterCriticalSection","winbase/TryEnterCriticalSection"]
old-location: base\tryentercriticalsection.htm
tech.root: base
ms.assetid: 5225bda1-6e20-4f6b-9f9b-633c62acfdce
ms.date: 12/05/2018
ms.keywords: TryEnterCriticalSection, TryEnterCriticalSection function, _win32_tryentercriticalsection, base.tryentercriticalsection, synchapi/TryEnterCriticalSection, winbase/TryEnterCriticalSection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TryEnterCriticalSection
 - synchapi/TryEnterCriticalSection
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
api_name:
 - TryEnterCriticalSection
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
<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a> function to initialize the object.

To enable mutually exclusive use of a shared resource, each thread calls the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection">EnterCriticalSection</a> or 
<b>TryEnterCriticalSection</b> function to request ownership of the critical section before executing any section of code that uses the protected resource. The difference is that 
<b>TryEnterCriticalSection</b> returns immediately, regardless of whether it obtained ownership of the critical section, while 
<b>EnterCriticalSection</b> blocks until the thread can take ownership of the critical section. When it has finished executing the protected code, the thread uses the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection">LeaveCriticalSection</a> function to relinquish ownership, enabling another thread to become the owner and gain access to the protected resource. The thread must call 
<b>LeaveCriticalSection</b> once for each time that it entered the critical section.

Any thread of the process can use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a> function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

If a thread terminates while it has ownership of a critical section, the state of the critical section is undefined.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Sync/critical-section-objects">Critical Section Objects</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection">EnterCriticalSection</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection">LeaveCriticalSection</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>