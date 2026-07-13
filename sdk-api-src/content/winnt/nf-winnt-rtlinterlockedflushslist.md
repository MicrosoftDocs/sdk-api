---
UID: NF:winnt.RtlInterlockedFlushSList
title: RtlInterlockedFlushSList function (winnt.h)
description: Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system. (RtlInterlockedFlushSList)
helpviewer_keywords: ["RtlInterlockedFlushSList","RtlInterlockedFlushSList function","base.rtlinterlockedflushslist","winnt/RtlInterlockedFlushSList"]
old-location: base\rtlinterlockedflushslist.htm
tech.root: backup
ms.assetid: bc5f28d8-c976-4614-9136-99887c617023
ms.date: 12/05/2018
ms.keywords: RtlInterlockedFlushSList, RtlInterlockedFlushSList function, base.rtlinterlockedflushslist, winnt/RtlInterlockedFlushSList
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
 - RtlInterlockedFlushSList
 - winnt/RtlInterlockedFlushSList
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
 - RtlInterlockedFlushSList
---

# RtlInterlockedFlushSList function


## -description

Removes all items from a singly linked list. Access to the list is synchronized on a multiprocessor system.

## -parameters

### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of the singly linked list. This structure is for system use only.

## -returns

The return value is a pointer to the items removed from the list. If the list is empty, the return value is <b>NULL</b>.

## -remarks

Calls to the <a href="/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist">InterlockedFlushSList</a> function are forwarded to the <b>RtlInterlockedFlushSList</b> function. Applications should call <b>InterlockedFlushSList</b> instead of calling this function directly.

## -see-also

<a href="/windows/desktop/Sync/interlocked-singly-linked-lists">Interlocked Singly Linked Lists</a>
