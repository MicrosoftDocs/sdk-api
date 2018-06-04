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

# _PSAPI_WORKING_SET_EX_INFORMATION structure


## -description


Contains extended working set information for a process.


## -struct-fields




### -field VirtualAddress

The virtual address.


### -field VirtualAttributes

A <a href="https://msdn.microsoft.com/4ba17fa0-2aed-4099-9380-fc13f1b826ca">PSAPI_WORKING_SET_EX_BLOCK</a> union that indicates the attributes of the page at <b>VirtualAddress</b>.


## -see-also




<a href="https://msdn.microsoft.com/4ba17fa0-2aed-4099-9380-fc13f1b826ca">PSAPI_WORKING_SET_EX_BLOCK</a>



<a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a>
 

 

