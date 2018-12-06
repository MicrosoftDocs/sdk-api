---
UID: NF:winnt.RtlFirstEntrySList
title: RtlFirstEntrySList function
author: windows-sdk-content
description: Retrieves the first entry in a singly linked list. Access to the list is synchronized on a multiprocessor system.
old-location: base\rtlfirstentryslist.htm
tech.root: sync
ms.assetid: 945d65a3-a2d2-4865-86ec-0ced0934dc1e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlFirstEntrySList, RtlFirstEntrySList function, base.rtlfirstentryslist, winnt/RtlFirstEntrySList
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
 - RtlFirstEntrySList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlFirstEntrySList function


## -description


Retrieves the first entry in a singly linked list. Access to the list is synchronized on a multiprocessor system.


## -parameters




### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a> function.


## -returns



The return value is a pointer to the first entry in the list. If the list is empty, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

