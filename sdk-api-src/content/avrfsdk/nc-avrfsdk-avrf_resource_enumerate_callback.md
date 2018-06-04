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

# AVRF_RESOURCE_ENUMERATE_CALLBACK callback function


## -description


Provides access to one of the specialized callback functions for enumeration of either heap allocation or handle trace information.


## -parameters




### -param ResourceDescription

A pointer to either an <a href="https://msdn.microsoft.com/9268d24d-5000-4ac5-a3c5-895613ccbb9a">AVRF_HANDLE_OPERATION</a> structure or an <a href="https://msdn.microsoft.com/238c7de7-4bf1-4974-8a6f-09e4d5f756ab">AVRF_HEAP_ALLOCATION</a> structure. Be sure to  cast this parameter to the correct structure type.


### -param EnumerationContext

A pointer to be passed to the resource-specific callback function.


### -param EnumerationLevel

Specifies whether the enumeration operation should continue. This must be one of the values in the <a href="https://msdn.microsoft.com/f8260ae8-eb1e-45f4-babc-905f4af7e3b1">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

