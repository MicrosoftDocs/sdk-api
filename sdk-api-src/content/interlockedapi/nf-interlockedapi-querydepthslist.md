---
UID: NF:interlockedapi.QueryDepthSList
title: QueryDepthSList function
author: windows-sdk-content
description: Retrieves the number of entries in the specified singly linked list.
old-location: base\querydepthslist.htm
old-project: sync
ms.assetid: 3f9b4481-647f-457f-bdfb-62e6ae4198e5
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: QueryDepthSList, QueryDepthSList function, base.querydepthslist, interlockedapi/QueryDepthSList, winbase/QueryDepthSList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: interlockedapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - QueryDepthSList
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# QueryDepthSList function


## -description


Retrieves the number of entries in the specified singly linked list.


## -parameters




### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a> function.


## -returns



The function returns the number of entries in the list, up to a maximum value of 65535. 




## -remarks



The system does not limit the number of entries in a singly linked list. However, the return value of <b>QueryDepthSList</b> is truncated to 16 bits, so the maximum value it can return is 65535. If the specified singly linked list contains more than 65535 entries, <b>QueryDepthSList</b> returns the number of entries in the list modulo 65535. For example, if the specified list contains 65536 entries, <b>QueryDepthSList</b> returns zero. 

The return value of <b>QueryDepthSList</b> should not be relied upon in multithreaded applications because the item count can be changed at any time by another thread. 




## -see-also




<a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a>



<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

