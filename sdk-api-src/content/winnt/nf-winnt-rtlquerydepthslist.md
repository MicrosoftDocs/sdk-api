---
UID: NF:winnt.RtlQueryDepthSList
title: RtlQueryDepthSList function (winnt.h)
description: Retrieves the number of entries in the specified singly linked list. (RtlQueryDepthSList)
helpviewer_keywords: ["RtlQueryDepthSList","RtlQueryDepthSList function","base.rtlquerydepthslist","winnt/RtlQueryDepthSList"]
old-location: base\rtlquerydepthslist.htm
tech.root: backup
ms.assetid: 5a73b181-e1ea-459a-b3b0-6cf16980930c
ms.date: 12/05/2018
ms.keywords: RtlQueryDepthSList, RtlQueryDepthSList function, base.rtlquerydepthslist, winnt/RtlQueryDepthSList
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
 - RtlQueryDepthSList
 - winnt/RtlQueryDepthSList
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
 - RtlQueryDepthSList
---

# RtlQueryDepthSList function


## -description

Retrieves the number of entries in the specified singly linked list.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a> function.

## -returns

The function returns the number of entries in the list.

## -remarks

Calls to the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-querydepthslist">QueryDepthSList</a> function are forwarded to the <b>RtlQueryDepthSList</b> function. Applications should call <b>QueryDepthSList</b> instead of calling this function directly.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>
