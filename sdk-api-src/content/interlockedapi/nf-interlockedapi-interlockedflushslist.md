---
UID: NF:interlockedapi.InterlockedFlushSList
title: InterlockedFlushSList function (interlockedapi.h)
description: Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system. (InterlockedFlushSList)
helpviewer_keywords: ["InterlockedFlushSList","InterlockedFlushSList function","_win32_interlockedflushslist","base.interlockedflushslist","interlockedapi/InterlockedFlushSList","winbase/InterlockedFlushSList"]
old-location: base\interlockedflushslist.htm
tech.root: backup
ms.assetid: 3fde3377-8a98-4976-a350-2c173b209e8c
ms.date: 02/02/2024
ms.keywords: InterlockedFlushSList, InterlockedFlushSList function, _win32_interlockedflushslist, base.interlockedflushslist, interlockedapi/InterlockedFlushSList, winbase/InterlockedFlushSList
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
 - InterlockedFlushSList
 - interlockedapi/InterlockedFlushSList
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
 - vertdll.dll
api_name:
 - InterlockedFlushSList
---

# InterlockedFlushSList function

## -description

Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in, out]

Pointer to an **SLIST_HEADER** structure that represents the head of the singly linked list. This structure is for system use only.

## -returns

The return value is a pointer to the items removed from the list. If the list is empty, the return value is `NULL`.

## -remarks

All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably. See **_aligned_malloc**.

#### Examples

For an example, see [Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists).

## -see-also

[Interlocked Singly Linked Lists](/windows/win32/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](nf-interlockedapi-interlockedpopentryslist.md)

[InterlockedPushEntrySList](nf-interlockedapi-interlockedpushentryslist.md)

[InterlockedPushListSList](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))

[InterlockedPushListSListEx](nf-interlockedapi-interlockedpushlistslistex.md)

[SLIST_ENTRY](../winnt/ns-winnt-slist_entry.md)

[Using Singly Linked Lists](/windows/win32/Sync/using-singly-linked-lists)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
