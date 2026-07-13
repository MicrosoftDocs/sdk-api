---
UID: NF:synchapi.TryEnterCriticalSection
title: TryEnterCriticalSection function (synchapi.h)
description: Attempts to enter a critical section without blocking. If the call is successful, the calling thread takes ownership of the critical section.
helpviewer_keywords: ["TryEnterCriticalSection","TryEnterCriticalSection function","_win32_tryentercriticalsection","base.tryentercriticalsection","synchapi/TryEnterCriticalSection","winbase/TryEnterCriticalSection"]
old-location: base\tryentercriticalsection.htm
tech.root: base
ms.assetid: 5225bda1-6e20-4f6b-9f9b-633c62acfdce
ms.date: 02/05/2024
ms.keywords: TryEnterCriticalSection, TryEnterCriticalSection function, _win32_tryentercriticalsection, base.tryentercriticalsection, synchapi/TryEnterCriticalSection, winbase/TryEnterCriticalSection
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
 - vertdll.dll
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

The threads of a single process can use a critical section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must call the [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) or [InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md) function to initialize the object.

To enable mutually exclusive use of a shared resource, each thread calls the [EnterCriticalSection](nf-synchapi-entercriticalsection.md) or **TryEnterCriticalSection** function to request ownership of the critical section before executing any section of code that uses the protected resource. The difference is that **TryEnterCriticalSection** returns immediately, regardless of whether it obtained ownership of the critical section, while **EnterCriticalSection** blocks until the thread can take ownership of the critical section. When it has finished executing the protected code, the thread uses the [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md) function to relinquish ownership, enabling another thread to become the owner and gain access to the protected resource. The thread must call **LeaveCriticalSection** once for each time that it entered the critical section.

Any thread of the process can use the [DeleteCriticalSection](nf-synchapi-deletecriticalsection.md) function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

If a thread terminates while it has ownership of a critical section, the state of the critical section is undefined.

To compile an application that uses this function, define **_WIN32_WINNT** as `0x0400` or later. For more information, see [Using the Windows Headers](/windows/win32/WinProg/using-the-windows-headers).

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[DeleteCriticalSection](nf-synchapi-deletecriticalsection.md)

[EnterCriticalSection](nf-synchapi-entercriticalsection.md)

[InitializeCriticalSection](nf-synchapi-initializecriticalsection.md)

[InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md)

[LeaveCriticalSection](nf-synchapi-leavecriticalsection.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
