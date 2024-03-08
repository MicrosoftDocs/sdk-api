---
UID: NF:interlockedapi.InitializeSListHead
title: InitializeSListHead function (interlockedapi.h)
description: Initializes the head of a singly linked list. (InitializeSListHead)
helpviewer_keywords: ["InitializeSListHead","InitializeSListHead function","_win32_initializeslisthead","base.initializeslisthead","interlockedapi/InitializeSListHead","winbase/InitializeSListHead"]
old-location: base\initializeslisthead.htm
tech.root: backup
ms.assetid: 4e34f947-1687-4ea9-aaa1-8d8dc11dad70
ms.date: 02/02/2024
ms.keywords: InitializeSListHead, InitializeSListHead function, _win32_initializeslisthead, base.initializeslisthead, interlockedapi/InitializeSListHead, winbase/InitializeSListHead
req.header: interlockedapi.h
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
 - InitializeSListHead
 - interlockedapi/InitializeSListHead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-interlocked-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-interlocked-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - Ntoskrnl.exe
 - vertdll.dll
api_name:
 - InitializeSListHead
---

# InitializeSListHead function

## -description

Initializes the head of a singly linked list.

## -parameters

### -param ListHead [in, out]

A pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list. This structure is for system use only.

## -remarks

All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary. Unaligned items can cause unpredictable results. See **_aligned_malloc**.

To add items to the list, use the [InterlockedPushEntrySList](nf-interlockedapi-interlockedpushentryslist.md) function. To remove items from the list, use the [InterlockedPopEntrySList](nf-interlockedapi-interlockedpopentryslist.md) function.

#### Examples

For an example, see [Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists).

## -see-also

[Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](nf-interlockedapi-interlockedpopentryslist.md)

[InterlockedPushEntrySList](nf-interlockedapi-interlockedpushentryslist.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
