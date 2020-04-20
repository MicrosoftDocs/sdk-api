---
UID: NS:winnt._SINGLE_LIST_ENTRY
title: SINGLE_LIST_ENTRY (winnt.h)
description: Represents an item in a singly linked list.helpviewer_keywords: ["*PSINGLE_LIST_ENTRY","*PSLIST_ENTRY","PSLIST_ENTRY","PSLIST_ENTRY structure pointer","SINGLE_LIST_ENTRY","SLIST_ENTRY","SLIST_ENTRY structure","_SLIST_ENTRY","_win32_slist_entry_str","base.slist_entry_str","winnt/PSLIST_ENTRY","winnt/SLIST_ENTRY"]
old-location: base\slist_entry_str.htm
tech.root: Sync
ms.assetid: 6c467621-fa51-49f1-b962-2dd5ec0f7084
ms.date: 12/05/2018
ms.keywords: '*PSINGLE_LIST_ENTRY, *PSLIST_ENTRY, PSLIST_ENTRY, PSLIST_ENTRY structure pointer, SINGLE_LIST_ENTRY, SLIST_ENTRY, SLIST_ENTRY structure, _SLIST_ENTRY, _win32_slist_entry_str, base.slist_entry_str, winnt/PSLIST_ENTRY, winnt/SLIST_ENTRY'
f1_keywords:
- winnt/SLIST_ENTRY
dev_langs:
- c++
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winnt.h
api_name:
- SLIST_ENTRY
targetos: Windows
req.typenames: SINGLE_LIST_ENTRY, *PSINGLE_LIST_ENTRY, SLIST_ENTRY, *PSLIST_ENTRY
req.redist: 
ms.custom: 19H1
---

# SINGLE_LIST_ENTRY structure


## -description


Represents an item in a singly linked list.


## -struct-fields




### -field Next

A pointer to an 
<b>SLIST_ENTRY</b> structure that represents the next item in a singly linked list.


## -remarks



All list items must be aligned on a  <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary. Unaligned items can cause unpredictable results. See <b>_aligned_malloc</b>.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist">InterlockedFlushSList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a>
 

 

