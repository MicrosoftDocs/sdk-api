---
UID: NF:winnt.RtlInterlockedPopEntrySList
title: RtlInterlockedPopEntrySList function (winnt.h)
description: Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (RtlInterlockedPopEntrySList)
helpviewer_keywords: ["RtlInterlockedPopEntrySList","RtlInterlockedPopEntrySList function","base.rtlinterlockedpopentryslist","winnt/RtlInterlockedPopEntrySList"]
old-location: base\rtlinterlockedpopentryslist.htm
tech.root: backup
ms.assetid: a3c14d28-627f-42e1-b149-04a333a2cde1
ms.date: 12/05/2018
ms.keywords: RtlInterlockedPopEntrySList, RtlInterlockedPopEntrySList function, base.rtlinterlockedpopentryslist, winnt/RtlInterlockedPopEntrySList
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
 - RtlInterlockedPopEntrySList
 - winnt/RtlInterlockedPopEntrySList
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
 - RtlInterlockedPopEntrySList
---

# RtlInterlockedPopEntrySList function


## -description

Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list.

## -returns

The return value is a pointer to the item removed from the list. If the list is empty, the return value is <b>NULL</b>.

## -remarks

Calls to the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist">InterlockedPopEntrySList</a> function are forwarded to the <b>RtlInterlockedPopEntrySList</b> function. Applications should call <b>InterlockedPopEntrySList</b> instead of calling this function directly.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>
