---
UID: NF:synchapi.LeaveCriticalSection
title: LeaveCriticalSection function (synchapi.h)
description: Releases ownership of the specified critical section object.
helpviewer_keywords: ["LeaveCriticalSection","LeaveCriticalSection function","_win32_leavecriticalsection","base.leavecriticalsection","synchapi/LeaveCriticalSection","winbase/LeaveCriticalSection"]
old-location: base\leavecriticalsection.htm
tech.root: base
ms.assetid: cf740e1d-351f-478c-bdbb-4a776b84acc5
ms.date: 02/05/2024
ms.keywords: LeaveCriticalSection, LeaveCriticalSection function, _win32_leavecriticalsection, base.leavecriticalsection, synchapi/LeaveCriticalSection, winbase/LeaveCriticalSection
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
 - LeaveCriticalSection
 - synchapi/LeaveCriticalSection
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
 - LeaveCriticalSection
---

# LeaveCriticalSection function

## -description

Releases ownership of the specified critical section object.

## -parameters

### -param lpCriticalSection [in, out]

A pointer to the critical section object.

## -remarks

The threads of a single process can use a critical-section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical-section object, which it can do by declaring a variable of type **CRITICAL_SECTION**. Before using a critical section, some thread of the process must call the [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) or [InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md) function to initialize the object.

A thread uses the [EnterCriticalSection](nf-synchapi-entercriticalsection.md) or [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md) function to acquire ownership of a critical section object. To release its ownership, the thread must call **LeaveCriticalSection** once for each time that it entered the critical section.

If a thread calls **LeaveCriticalSection** when it does not have ownership of the specified critical section object, an error occurs that may cause another thread using [EnterCriticalSection](nf-synchapi-entercriticalsection.md) to wait indefinitely.

**LeaveCriticalSection** does not access the specified **CRITICAL_SECTION** structure after the ownership of a critical section object is released.

Any thread of the process can use the [DeleteCriticalSection](nf-synchapi-deletecriticalsection.md) function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.

#### Examples

For an example that uses **LeaveCriticalSection**, see [Using Critical Section Objects](/windows/win32/Sync/using-critical-section-objects).

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[DeleteCriticalSection](nf-synchapi-deletecriticalsection.md)

[EnterCriticalSection](nf-synchapi-entercriticalsection.md)

[InitializeCriticalSection](nf-synchapi-initializecriticalsection.md)

[InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
