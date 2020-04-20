---
UID: NF:interlockedapi.InterlockedFlushSList
title: InterlockedFlushSList function (interlockedapi.h)
description: Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system.helpviewer_keywords: ["InterlockedFlushSList","InterlockedFlushSList function","_win32_interlockedflushslist","base.interlockedflushslist","interlockedapi/InterlockedFlushSList","winbase/InterlockedFlushSList"]
old-location: base\interlockedflushslist.htm
tech.root: Sync
ms.assetid: 3fde3377-8a98-4976-a350-2c173b209e8c
ms.date: 12/05/2018
ms.keywords: InterlockedFlushSList, InterlockedFlushSList function, _win32_interlockedflushslist, base.interlockedflushslist, interlockedapi/InterlockedFlushSList, winbase/InterlockedFlushSList
f1_keywords:
- interlockedapi/InterlockedFlushSList
dev_langs:
- c++
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
api_name:
- InterlockedFlushSList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedFlushSList function


## -description


Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system.


## -parameters




### -param ListHead [in, out]

Pointer to an <b>SLIST_HEADER</b> structure that represents the head of the singly linked list. This structure is for system use only.


## -returns



The return value is a pointer to the items removed from the list. If the list is empty, the return value is <b>NULL</b>.




## -remarks



All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448545(v=vs.85)">InterlockedPushListSList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex">InterlockedPushListSListEx</a>



<a href="/windows/desktop/api/winnt/ns-winnt-_list_entry">SLIST_ENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>
 

 

