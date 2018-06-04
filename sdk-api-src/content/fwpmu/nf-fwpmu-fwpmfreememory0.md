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

# FwpmFreeMemory0 function


## -description


The <b>FwpmFreeMemory0</b> function is used to release memory resources allocated by the Windows Filtering Platform (WFP) functions.


## -parameters




### -param p [in, out]

Type: <b>void**</b>

Address of the pointer to be freed.


## -returns



This function does not return a value.




## -remarks



<b>FwpmFreeMemory0</b> is used to free memory returned by the various <b>Fwpm*</b> functions, such as <b>FwpmFilterGetByKey0</b>.

<b>Fwpm*</b> functions that return a HANDLE, such as <b>FwpmCalloutCreateEnumHandle0</b>, have specific functions to release memory.

If the caller passes a pointer that is not valid, the behavior is undefined.

<b>FwpmFreeMemory0</b> is a specific implementation of FwpmFreeMemory. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>



<a href="https://msdn.microsoft.com/e63db9e6-af26-4511-99fa-7d0b13d409d8">Windows Filtering Platform  API Reference</a>
 

 

