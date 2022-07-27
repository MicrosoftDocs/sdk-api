---
UID: NF:interlockedapi.InterlockedPushEntrySList
title: InterlockedPushEntrySList function (interlockedapi.h)
description: Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (InterlockedPushEntrySList)
helpviewer_keywords: ["InterlockedPushEntrySList","InterlockedPushEntrySList function","_win32_interlockedpushentryslist","base.interlockedpushentryslist","interlockedapi/InterlockedPushEntrySList","winbase/InterlockedPushEntrySList"]
old-location: base\interlockedpushentryslist.htm
tech.root: backup
ms.assetid: 60e3b6f7-f556-4699-be90-db7330cfb8ca
ms.date: 12/05/2018
ms.keywords: InterlockedPushEntrySList, InterlockedPushEntrySList function, _win32_interlockedpushentryslist, base.interlockedpushentryslist, interlockedapi/InterlockedPushEntrySList, winbase/InterlockedPushEntrySList
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

Pointer to an 
<a href="/windows/win32/api/winnt/ns-winnt-slist_entry">SLIST_ENTRY</a> structure that represents an item in a singly linked list.

## -returns

The return value is the previous first item in the list. If the list was previously empty, the return value is <b>NULL</b>.

## -remarks

All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist">InterlockedFlushSList</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a>



<a href="/previous-versions/windows/desktop/legacy/hh448545(v=vs.85)">InterlockedPushListSList</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex">InterlockedPushListSListEx</a>



<a href="/windows/win32/api/winnt/ns-winnt-slist_entry">SLIST_ENTRY</a>



<a href="/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>
