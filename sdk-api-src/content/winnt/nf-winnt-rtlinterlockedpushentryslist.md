---
UID: NF:winnt.RtlInterlockedPushEntrySList
title: RtlInterlockedPushEntrySList function (winnt.h)
description: Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system. (RtlInterlockedPushEntrySList)
helpviewer_keywords: ["RtlInterlockedPushEntrySList","RtlInterlockedPushEntrySList function","base.rtlinterlockedpushentryslist","winnt/RtlInterlockedPushEntrySList"]
old-location: base\rtlinterlockedpushentryslist.htm
tech.root: backup
ms.assetid: 0d52bc3a-9f43-4bc2-99c2-1a0efa7b29cd
ms.date: 12/05/2018
ms.keywords: RtlInterlockedPushEntrySList, RtlInterlockedPushEntrySList function, base.rtlinterlockedpushentryslist, winnt/RtlInterlockedPushEntrySList
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
 - RtlInterlockedPushEntrySList
 - winnt/RtlInterlockedPushEntrySList
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
 - RtlInterlockedPushEntrySList
---

# RtlInterlockedPushEntrySList function


## -description

Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list.

### -param ListEntry [in]

A pointer to an 
[SLIST_ENTRY](./ns-winnt-slist_entry.md) structure that represents an item in a singly linked list.

## -returns

The return value is the previous first item in the list. If the list was previously empty, the return value is <b>NULL</b>.

## -remarks

Calls to the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist">InterlockedPushEntrySList</a> function are forwarded to the <b>RtlInterlockedPushEntrySList</b> function. Applications should call <b>InterlockedPushEntrySList</b> instead of calling this function directly.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>
