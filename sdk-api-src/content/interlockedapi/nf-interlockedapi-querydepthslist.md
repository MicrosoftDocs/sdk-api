---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# QueryDepthSList function


## -description


Retrieves the number of entries in the specified singly linked list.


## -parameters




### -param ListHead [in]

A pointer to an <b>SLIST_HEADER</b> structure that represents the head of a singly linked list. This structure is for system use only. 

The list must  be previously initialized with the <a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a> function.


## -returns



The function returns the number of entries in the list, up to a maximum value of 65535. 




## -remarks



The system does not limit the number of entries in a singly linked list. However, the return value of <b>QueryDepthSList</b> is truncated to 16 bits, so the maximum value it can return is 65535. If the specified singly linked list contains more than 65535 entries, <b>QueryDepthSList</b> returns the number of entries in the list modulo 65535. For example, if the specified list contains 65536 entries, <b>QueryDepthSList</b> returns zero. 

The return value of <b>QueryDepthSList</b> should not be relied upon in multithreaded applications because the item count can be changed at any time by another thread. 




## -see-also




<a href="https://msdn.microsoft.com/4e34f947-1687-4ea9-aaa1-8d8dc11dad70">InitializeSListHead</a>



<a href="https://msdn.microsoft.com/35463ace-33ab-4eb9-9901-2504a92456e2">Interlocked Singly Linked Lists</a>
 

 

