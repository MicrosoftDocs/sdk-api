---
UID: NF:winnt.RtlFirstEntrySList
title: RtlFirstEntrySList function (winnt.h)
description: Retrieves the first entry in a singly linked list. Access to the list is synchronized on a multiprocessor system.
helpviewer_keywords: ["RtlFirstEntrySList","RtlFirstEntrySList function","base.rtlfirstentryslist","winnt/RtlFirstEntrySList"]
old-location: base\rtlfirstentryslist.htm
tech.root: backup
ms.assetid: 945d65a3-a2d2-4865-86ec-0ced0934dc1e
ms.date: 12/05/2018
ms.keywords: RtlFirstEntrySList, RtlFirstEntrySList function, base.rtlfirstentryslist, winnt/RtlFirstEntrySList
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlFirstEntrySList
 - winnt/RtlFirstEntrySList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlFirstEntrySList
---

# RtlFirstEntrySList function


## -description

Retrieves the first entry in a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a> function.

## -returns

The return value is a pointer to the first entry in the list. If the list is empty, the return value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>