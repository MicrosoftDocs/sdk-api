---
UID: NF:interlockedapi.InterlockedPopEntrySList
title: InterlockedPopEntrySList function (interlockedapi.h)
description: Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (InterlockedPopEntrySList)
helpviewer_keywords: ["InterlockedPopEntrySList","InterlockedPopEntrySList function","_win32_interlockedpopentryslist","base.interlockedpopentryslist","interlockedapi/InterlockedPopEntrySList","winbase/InterlockedPopEntrySList"]
old-location: base\interlockedpopentryslist.htm
tech.root: backup
ms.assetid: 10760fd4-5973-4ab0-991c-7a5951c798a4
ms.date: 02/02/2024
ms.keywords: InterlockedPopEntrySList, InterlockedPopEntrySList function, _win32_interlockedpopentryslist, base.interlockedpopentryslist, interlockedapi/InterlockedPopEntrySList, winbase/InterlockedPopEntrySList
req.header: interlockedapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - InterlockedPopEntrySList
 - interlockedapi/InterlockedPopEntrySList
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
 - InterlockedPopEntrySList
---

# InterlockedPopEntrySList function

## -description

Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in, out]

Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.

## -returns

The return value is a pointer to the item removed from the list. If the list is empty, the return value is `NULL`.

## -remarks

All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably. See **_aligned_malloc**.

#### Examples

For an example, see [Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists).

## -see-also

[Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists)

[InterlockedFlushSList](nf-interlockedapi-interlockedflushslist.md)

[InterlockedPushEntrySList](nf-interlockedapi-interlockedpushentryslist.md)

[InterlockedPushListSList](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))

[InterlockedPushListSListEx](nf-interlockedapi-interlockedpushlistslistex.md)

[SLIST_ENTRY](../winnt/ns-winnt-slist_entry.md)

[Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
