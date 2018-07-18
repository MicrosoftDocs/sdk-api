---
UID: NF:interlockedapi.InterlockedPushListSListEx
title: InterlockedPushListSListEx function
author: windows-sdk-content
description: Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the __fastcall calling convention.
old-location: base\interlockedpushlistslistex.htm
old-project: sync
ms.assetid: f4f334c6-fda8-4c5f-9177-b672c8aed6b3
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: InterlockedPushListSListEx, InterlockedPushListSListEx function, base.interlockedpushlistslistex, interlockedapi/InterlockedPushListSListEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: interlockedapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-interlocked-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - InterlockedPushListSListEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# InterlockedPushListSListEx function


## -description


Inserts a singly-linked list at the front of another singly linked list. Access to the lists is synchronized on a multiprocessor system. This version of the method does not use the <a href="bb5b9c8a-dfad-450c-9119-0ac2bc59544f">__fastcall</a> calling convention.


## -parameters




### -param ListHead [in, out]

Pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. The list specified by the <i>List</i> and <i>ListEnd</i> parameters is inserted at the front of this list.


### -param List [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563805">SLIST_ENTRY</a> structure that represents the first item in the  list to be inserted. 


### -param ListEnd [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563805">SLIST_ENTRY</a> structure that represents the last item in the  list to be inserted. 


### -param Count [in]

The number of items in the list to be inserted.


## -returns



The return value is the previous first item in the list specified by the <i>ListHead</i> parameter. If the list was previously empty, the return value is <b>NULL</b>.




## -remarks



All list items must be aligned on a <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary; otherwise, this function will behave unpredictably. See <b>_aligned_malloc</b>. 




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>



<a href="https://msdn.microsoft.com/3fde3377-8a98-4976-a350-2c173b209e8c">InterlockedFlushSList</a>



<a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a>



<a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563805">SLIST_ENTRY</a>



<a href="https://msdn.microsoft.com/5608f84f-9211-4043-bb53-60339191ee29">Using Singly Linked Lists</a>
 

 

