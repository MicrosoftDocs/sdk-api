---
UID: NF:winnt.RtlInitializeSListHead
title: RtlInitializeSListHead function
author: windows-sdk-content
description: Initializes the head of a singly linked list.
old-location: base\rtlinitializeslisthead.htm
tech.root: Sync
ms.assetid: 0f5467e0-6fba-418d-8f00-cb4fa475f7e2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RtlInitializeSListHead, RtlInitializeSListHead function, base.rtlinitializeslisthead, winnt/RtlInitializeSListHead
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
 - RtlInitializeSListHead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtlInitializeSListHead
: 
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



Calls to the <a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a> function are forwarded to the <b>RtlInitializeSListHead</b> function. Applications should call <b>InitializeSListHead</b> instead of calling this function directly.




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

