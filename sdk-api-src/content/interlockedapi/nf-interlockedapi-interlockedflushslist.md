---
UID: NF:interlockedapi.InterlockedFlushSList
title: InterlockedFlushSList function
author: windows-sdk-content
description: Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system.
old-location: base\interlockedflushslist.htm
old-project: Sync
ms.assetid: 3fde3377-8a98-4976-a350-2c173b209e8c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: InterlockedFlushSList, InterlockedFlushSList function, _win32_interlockedflushslist, base.interlockedflushslist, interlockedapi/InterlockedFlushSList, winbase/InterlockedFlushSList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: interlockedapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/5608f84f-9211-4043-bb53-60339191ee29">Using Singly Linked Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>



<a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a>



<a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a>



<a href="https://msdn.microsoft.com/19c2ec08-324d-4d41-b8ac-5fab59655106">InterlockedPushListSList</a>



<a href="https://msdn.microsoft.com/f4f334c6-fda8-4c5f-9177-b672c8aed6b3">InterlockedPushListSListEx</a>



<a href="https://msdn.microsoft.com/6c467621-fa51-49f1-b962-2dd5ec0f7084">SLIST_ENTRY</a>



<a href="https://msdn.microsoft.com/5608f84f-9211-4043-bb53-60339191ee29">Using Singly Linked Lists</a>
 

 

