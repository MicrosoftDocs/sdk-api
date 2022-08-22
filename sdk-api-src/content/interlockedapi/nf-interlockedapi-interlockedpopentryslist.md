---
UID: NF:interlockedapi.InterlockedPopEntrySList
title: InterlockedPopEntrySList function (interlockedapi.h)
description: Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (InterlockedPopEntrySList)
helpviewer_keywords: ["InterlockedPopEntrySList","InterlockedPopEntrySList function","_win32_interlockedpopentryslist","base.interlockedpopentryslist","interlockedapi/InterlockedPopEntrySList","winbase/InterlockedPopEntrySList"]
old-location: base\interlockedpopentryslist.htm
tech.root: backup
ms.assetid: 10760fd4-5973-4ab0-991c-7a5951c798a4
ms.date: 12/05/2018
ms.keywords: InterlockedPopEntrySList, InterlockedPopEntrySList function, _win32_interlockedpopentryslist, base.interlockedpopentryslist, interlockedapi/InterlockedPopEntrySList, winbase/InterlockedPopEntrySList
req.header: interlockedapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
api_name:
 - InterlockedPopEntrySList
---

# InterlockedPopEntrySList function


## -description

Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in, out]

Pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list.

## -returns

The return value is a pointer to the item removed from the list. If the list is empty, the return value is <b>NULL</b>.

## -remarks

All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist">InterlockedFlushSList</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a>



<a href="/previous-versions/windows/desktop/legacy/hh448545(v=vs.85)">InterlockedPushListSList</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex">InterlockedPushListSListEx</a>



<a href="/windows/win32/api/winnt/ns-winnt-slist_entry">SLIST_ENTRY</a>



<a href="/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>
