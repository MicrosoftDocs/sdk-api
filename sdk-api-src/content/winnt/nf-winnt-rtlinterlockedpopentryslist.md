---
UID: NF:winnt.RtlInterlockedPopEntrySList
title: RtlInterlockedPopEntrySList function
author: windows-sdk-content
description: Removes an item from the front of a singly linked list. Access to the list is synchronized on a multiprocessor system.
old-location: base\rtlinterlockedpopentryslist.htm
tech.root: sync
ms.assetid: a3c14d28-627f-42e1-b149-04a333a2cde1
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: RtlInterlockedPopEntrySList, RtlInterlockedPopEntrySList function, base.rtlinterlockedpopentryslist, winnt/RtlInterlockedPopEntrySList
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlInterlockedPopEntrySList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Calls to the <a href="https://msdn.microsoft.com/10760fd4-5973-4ab0-991c-7a5951c798a4">InterlockedPopEntrySList</a> function are forwarded to the <b>RtlInterlockedPopEntrySList</b> function. Applications should call <b>InterlockedPopEntrySList</b> instead of calling this function directly.




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

