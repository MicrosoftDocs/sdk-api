---
UID: NF:interlockedapi.InitializeSListHead
title: InitializeSListHead function (interlockedapi.h)
description: Initializes the head of a singly linked list.
helpviewer_keywords: ["InitializeSListHead","InitializeSListHead function","_win32_initializeslisthead","base.initializeslisthead","interlockedapi/InitializeSListHead","winbase/InitializeSListHead"]
old-location: base\initializeslisthead.htm
tech.root: backup
ms.assetid: 4e34f947-1687-4ea9-aaa1-8d8dc11dad70
ms.date: 12/05/2018
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

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only.

## -remarks

All list items must be aligned on a  <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary. Unaligned items can cause unpredictable results. See <b>_aligned_malloc</b>.

To add items to the list, use the 
<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a> function. To remove items from the list, use the 
<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/using-singly-linked-lists">Using Singly Linked Lists</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a>



<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a>