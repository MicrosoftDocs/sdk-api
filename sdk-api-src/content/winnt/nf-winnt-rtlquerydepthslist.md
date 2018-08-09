---
UID: NF:winnt.RtlQueryDepthSList
title: RtlQueryDepthSList function
author: windows-sdk-content
description: Retrieves the number of entries in the specified singly linked list.
old-location: base\rtlquerydepthslist.htm
old-project: sync
ms.assetid: 5a73b181-e1ea-459a-b3b0-6cf16980930c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RtlQueryDepthSList, RtlQueryDepthSList function, base.rtlquerydepthslist, winnt/RtlQueryDepthSList
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
 - RtlQueryDepthSList
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
---

# RtlQueryDepthSList function


## -description


Retrieves the number of entries in the specified singly linked list.


## -parameters




### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a> function.


## -returns



The function returns the number of entries in the list.




## -remarks



Calls to the <a href="https://msdn.microsoft.com/3f9b4481-647f-457f-bdfb-62e6ae4198e5">QueryDepthSList</a> function are forwarded to the <b>RtlQueryDepthSList</b> function. Applications should call <b>QueryDepthSList</b> instead of calling this function directly.




## -see-also




<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

