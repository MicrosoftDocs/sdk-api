---
UID: NF:interlockedapi.InitializeSListHead
title: InitializeSListHead function
author: windows-sdk-content
description: Initializes the head of a singly linked list.
old-location: base\initializeslisthead.htm
old-project: Sync
ms.assetid: 4e34f947-1687-4ea9-aaa1-8d8dc11dad70
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: InitializeSListHead, InitializeSListHead function, _win32_initializeslisthead, base.initializeslisthead, interlockedapi/InitializeSListHead, winbase/InitializeSListHead
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: interlockedapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-interlocked-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-interlocked-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	Ntoskrnl.exe
api_name:
-	InitializeSListHead
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# InitializeSListHead function


## -description


Initializes the head of a singly linked list.


## -parameters




### -param ListHead [in, out]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only.


## -returns



This function does not return a value.




## -remarks



All list items must be aligned on a  <b>MEMORY_ALLOCATION_ALIGNMENT</b> boundary. Unaligned items can cause unpredictable results. See <b>_aligned_malloc</b>.

To add items to the list, use the 
<a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a> function. To remove items from the list, use the 
<a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5608f84f-9211-4043-bb53-60339191ee29">Using Singly Linked Lists</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>



<a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a>



<a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a>
 

 

