---
UID: NF:synchapi.InitializeCriticalSection
title: InitializeCriticalSection function (synchapi.h)
description: Initializes a critical section object.
helpviewer_keywords: ["InitializeCriticalSection","InitializeCriticalSection function","_win32_initializecriticalsection","base.initializecriticalsection","synchapi/InitializeCriticalSection","winbase/InitializeCriticalSection"]
old-location: base\initializecriticalsection.htm
tech.root: base
ms.assetid: ad4b182d-a65d-4890-9eda-fdd6d044f736
ms.date: 02/05/2024
ms.keywords: InitializeCriticalSection, InitializeCriticalSection function, _win32_initializecriticalsection, base.initializecriticalsection, synchapi/InitializeCriticalSection, winbase/InitializeCriticalSection
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
 - InitializeCriticalSection
 - synchapi/InitializeCriticalSection
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
 - InitializeCriticalSection
---

# InitializeCriticalSection function

## -description

Initializes a critical section object.

## -parameters

### -param lpCriticalSection [out]

A pointer to the critical section object.

## -returns

This function does not return a value.

**Windows Server 2003 and Windows XP:** In low memory situations, **InitializeCriticalSection** can raise a **STATUS_NO_MEMORY** exception. Starting with Windows Vista, this exception was eliminated and **InitializeCriticalSection** always succeeds, even in low memory situations.

## -remarks

The threads of a single process can use a critical section object for mutual-exclusion synchronization. There is no guarantee about the order in which threads will obtain ownership of the critical section, however, the system will be fair to all threads.

The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must initialize the object.

After a critical section object has been initialized, the threads of the process can specify the object in the [EnterCriticalSection](nf-synchapi-entercriticalsection.md), [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md), or [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md) function to provide mutually exclusive access to a shared resource. For similar synchronization between the threads of different processes, use a mutex object.

A critical section object cannot be moved or copied. The process must also not modify the object, but must treat it as logically opaque. Use only the critical section functions to manage critical section objects. When you have finished using the critical section, call the [DeleteCriticalSection](nf-synchapi-deletecriticalsection.md) function.

A critical section object must be deleted before it can be reinitialized. Initializing a critical section that has already been initialized results in undefined behavior.

## -see-also

[CreateMutex](nf-synchapi-createmutexa.md)

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[DeleteCriticalSection](nf-synchapi-deletecriticalsection.md)

[EnterCriticalSection](nf-synchapi-entercriticalsection.md)

[InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md)

[LeaveCriticalSection](nf-synchapi-leavecriticalsection.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
