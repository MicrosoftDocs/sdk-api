---
UID: NS:winnt._SINGLE_LIST_ENTRY
title: "_SINGLE_LIST_ENTRY"
author: windows-sdk-content
description: Represents an item in a singly linked list.
old-location: base\slist_entry_str.htm
tech.root: Sync
ms.assetid: 6c467621-fa51-49f1-b962-2dd5ec0f7084
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PSINGLE_LIST_ENTRY, *PSLIST_ENTRY, PSLIST_ENTRY, PSLIST_ENTRY structure pointer, SINGLE_LIST_ENTRY, SLIST_ENTRY, SLIST_ENTRY structure, _SINGLE_LIST_ENTRY, _SLIST_ENTRY, _win32_slist_entry_str, base.slist_entry_str, winnt/PSLIST_ENTRY, winnt/SLIST_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SINGLE_LIST_ENTRY, *PSINGLE_LIST_ENTRY, SLIST_ENTRY, *PSLIST_ENTRY
req.redist: 
---

# _SINGLE_LIST_ENTRY structure


## -description


Represents an item in a singly linked list.


## -struct-fields




#### - Next

A pointer to an 
<b>SLIST_ENTRY</b> structure that represents the next item in a singly linked list.


## -remarks



All list items must be aligned on a  <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary. Unaligned items can cause unpredictable results. See <b>_aligned_malloc</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5608f84f-9211-4043-bb53-60339191ee29">Using Singly Linked Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a>



<a href="https://msdn.microsoft.com/3fde3377-8a98-4976-a350-2c173b209e8c">InterlockedFlushSList</a>



<a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a>



<a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a>
 

 

