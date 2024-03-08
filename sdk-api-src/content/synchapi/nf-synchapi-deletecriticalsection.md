---
UID: NF:synchapi.DeleteCriticalSection
title: DeleteCriticalSection function (synchapi.h)
description: Releases all resources used by an unowned critical section object.
helpviewer_keywords: ["DeleteCriticalSection","DeleteCriticalSection function","_win32_deletecriticalsection","base.deletecriticalsection","synchapi/DeleteCriticalSection","winbase/DeleteCriticalSection"]
old-location: base\deletecriticalsection.htm
tech.root: base
ms.assetid: 97e29fc3-b155-448e-aaa9-19f0fc2d841e
ms.date: 02/05/2024
ms.keywords: DeleteCriticalSection, DeleteCriticalSection function, _win32_deletecriticalsection, base.deletecriticalsection, synchapi/DeleteCriticalSection, winbase/DeleteCriticalSection
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
 - DeleteCriticalSection
 - synchapi/DeleteCriticalSection
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
 - DeleteCriticalSection
---

# DeleteCriticalSection function

## -description

Releases all resources used by an unowned critical section object.

## -parameters

### -param lpCriticalSection [in, out]

A pointer to the critical section object. The object must have been previously initialized with the [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) function.

## -remarks

Deleting a critical section object releases all system resources used by the object. The caller is responsible for ensuring that the critical section object is unowned and the specified CRITICAL_SECTION structure is not being accessed by any critical section functions called by other threads in the process.

After a critical section object has been deleted, do not reference the object in any function that operates on critical sections (such as [EnterCriticalSection](nf-synchapi-entercriticalsection.md), [TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md), and [LeaveCriticalSection](nf-synchapi-leavecriticalsection.md)) other than [InitializeCriticalSection](nf-synchapi-initializecriticalsection.md) and [InitializeCriticalSectionAndSpinCount](nf-synchapi-initializecriticalsectionandspincount.md). If you attempt to do so, memory corruption and other unexpected errors can occur.

If a critical section is deleted while it is still owned, the state of the threads waiting for ownership of the deleted critical section is undefined.

#### Examples

For an example that uses **DeleteCriticalSection**, see [Using Critical Section Objects](/windows/win32/Sync/using-critical-section-objects).

## -see-also

[Critical Section Objects](/windows/win32/Sync/critical-section-objects)

[EnterCriticalSection](nf-synchapi-entercriticalsection.md)

[InitializeCriticalSection](nf-synchapi-initializecriticalsection.md)

[LeaveCriticalSection](nf-synchapi-leavecriticalsection.md)

[Synchronization Functions](/windows/win32/Sync/synchronization-functions)

[TryEnterCriticalSection](nf-synchapi-tryentercriticalsection.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
