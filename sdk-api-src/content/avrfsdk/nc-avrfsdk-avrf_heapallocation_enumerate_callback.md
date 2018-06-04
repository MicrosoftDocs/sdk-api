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

# AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function


## -description


Receives information related to heap allocations.


## -parameters




### -param HeapAllocation

A pointer to an <a href="https://msdn.microsoft.com/238c7de7-4bf1-4974-8a6f-09e4d5f756ab">AVRF_HEAP_ALLOCATION</a> structure containing information about the heap to be enumerated.


### -param EnumerationContext

A pointer to user-defined information in the context of the enumeration that is passed in when the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function is invoked.


### -param EnumerationLevel

A pointer to a value that informs the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function to either continue or stop the enumeration operation. These values are defined in the <a href="https://msdn.microsoft.com/f8260ae8-eb1e-45f4-babc-905f4af7e3b1">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>
 

 

