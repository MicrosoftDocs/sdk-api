---
UID: NF:winnt.RtlInterlockedPushEntrySList
title: RtlInterlockedPushEntrySList function
author: windows-sdk-content
description: Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.
old-location: base\rtlinterlockedpushentryslist.htm
old-project: sync
ms.assetid: 0d52bc3a-9f43-4bc2-99c2-1a0efa7b29cd
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: RtlInterlockedPushEntrySList, RtlInterlockedPushEntrySList function, base.rtlinterlockedpushentryslist, winnt/RtlInterlockedPushEntrySList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlInterlockedPushEntrySList
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlInterlockedPushEntrySList function


## -description


Inserts an item at the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.


## -parameters




### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list.


### -param ListEntry [in]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563805">SLIST_ENTRY</a> structure that represents an item in a singly linked list.


## -returns



The return value is the previous first item in the list. If the list was previously empty, the return value is <b>NULL</b>.




## -remarks



Calls to the <a href="https://msdn.microsoft.com/60e3b6f7-f556-4699-be90-db7330cfb8ca">InterlockedPushEntrySList</a> function are forwarded to the <b>RtlInterlockedPushEntrySList</b> function. Applications should call <b>InterlockedPushEntrySList</b> instead of calling this function directly.




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

