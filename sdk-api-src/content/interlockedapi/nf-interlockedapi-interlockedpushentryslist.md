---
UID: NF:interlockedapi.InterlockedPushEntrySList
title: InterlockedPushEntrySList function (interlockedapi.h)
description: Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (InterlockedPushEntrySList)
helpviewer_keywords: ["InterlockedPushEntrySList","InterlockedPushEntrySList function","_win32_interlockedpushentryslist","base.interlockedpushentryslist","interlockedapi/InterlockedPushEntrySList","winbase/InterlockedPushEntrySList"]
old-location: base\interlockedpushentryslist.htm
tech.root: backup
ms.assetid: 60e3b6f7-f556-4699-be90-db7330cfb8ca
ms.date: 02/02/2024
ms.keywords: InterlockedPushEntrySList, InterlockedPushEntrySList function, _win32_interlockedpushentryslist, base.interlockedpushentryslist, interlockedapi/InterlockedPushEntrySList, winbase/InterlockedPushEntrySList
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
 - InterlockedPushEntrySList
 - interlockedapi/InterlockedPushEntrySList
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
 - InterlockedPushEntrySList
---

# InterlockedPushEntrySList function

## -description

Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in, out]

Pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list.

### -param ListEntry [in, out]

Pointer to an [SLIST_ENTRY](../winnt/ns-winnt-slist_entry.md) structure that represents an item in a singly linked list.

## -returns

The return value is the previous first item in the list. If the list was previously empty, the return value is <b>NULL</b>.

## -remarks

All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>.

#### Examples

For an example, see [Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists).

## -see-also

[Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists)

[InterlockedFlushSList](nf-interlockedapi-interlockedflushslist.md)

[InterlockedPopEntrySList](nf-interlockedapi-interlockedpopentryslist.md)

[InterlockedPushListSList](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))

[InterlockedPushListSListEx](nf-interlockedapi-interlockedpushlistslistex.md)

[SLIST_ENTRY](../winnt/ns-winnt-slist_entry.md)

[Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
