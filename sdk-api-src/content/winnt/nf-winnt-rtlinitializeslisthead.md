---
UID: NF:winnt.RtlInitializeSListHead
title: RtlInitializeSListHead function (winnt.h)
description: Initializes the head of a singly linked list. (RtlInitializeSListHead)
helpviewer_keywords: ["RtlInitializeSListHead","RtlInitializeSListHead function","base.rtlinitializeslisthead","winnt/RtlInitializeSListHead"]
old-location: base\rtlinitializeslisthead.htm
tech.root: backup
ms.assetid: 0f5467e0-6fba-418d-8f00-cb4fa475f7e2
ms.date: 12/05/2018
ms.keywords: RtlInitializeSListHead, RtlInitializeSListHead function, base.rtlinitializeslisthead, winnt/RtlInitializeSListHead
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
 - RtlInitializeSListHead
 - winnt/RtlInitializeSListHead
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
 - RtlInitializeSListHead
---

# RtlInitializeSListHead function


## -description

Initializes the head of a singly linked list.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only.

## -returns

This function does not return a value.

## -remarks

Calls to the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-initializeslisthead">InitializeSListHead</a> function are forwarded to the <b>RtlInitializeSListHead</b> function. Applications should call <b>InitializeSListHead</b> instead of calling this function directly.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>
