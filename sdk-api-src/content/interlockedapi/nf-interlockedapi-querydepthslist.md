---
UID: NF:interlockedapi.QueryDepthSList
title: QueryDepthSList function (interlockedapi.h)
description: Retrieves the number of entries in the specified singly linked list.
helpviewer_keywords: ["QueryDepthSList","QueryDepthSList function","base.querydepthslist","interlockedapi/QueryDepthSList","winbase/QueryDepthSList"]
old-location: base\querydepthslist.htm
tech.root: backup
ms.assetid: 3f9b4481-647f-457f-bdfb-62e6ae4198e5
ms.date: 12/05/2018
ms.keywords: QueryDepthSList, QueryDepthSList function, base.querydepthslist, interlockedapi/QueryDepthSList, winbase/QueryDepthSList
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
 - QueryDepthSList
 - interlockedapi/QueryDepthSList
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
api_name:
 - QueryDepthSList
---

# QueryDepthSList function


## -description

Retrieves the number of entries in the specified singly linked list.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a> function.

## -returns

The function returns the number of entries in the list, up to a maximum value of 65535.

## -remarks

The system does not limit the number of entries in a singly linked list. However, the return value of <b>QueryDepthSList</b> is truncated to 16 bits, so the maximum value it can return is 65535. If the specified singly linked list contains more than 65535 entries, <b>QueryDepthSList</b> returns the number of entries in the list modulo 65535. For example, if the specified list contains 65536 entries, <b>QueryDepthSList</b> returns zero. 

The return value of <b>QueryDepthSList</b> should not be relied upon in multithreaded applications because the item count can be changed at any time by another thread.

## -see-also

<a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a>



<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>