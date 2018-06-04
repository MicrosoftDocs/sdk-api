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

# _PDH_FMT_COUNTERVALUE_ITEM_A structure


## -description



			The 
<b>PDH_FMT_COUNTERVALUE_ITEM</b> structure contains the instance name and formatted value of a counter.
		


## -struct-fields




### -field szName

Pointer to a null-terminated string that specifies the instance name of the counter. The string is appended to the end of this structure.


### -field FmtValue

 A <a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a> structure that contains the counter value of the instance.


## -see-also




<a href="https://msdn.microsoft.com/68ccd722-94d2-4610-ba64-f51318f5436e">PDH_FMT_COUNTERVALUE</a>



<a href="https://msdn.microsoft.com/0f388c7e-d0c8-461d-908c-48af92166996">PdhGetFormattedCounterArray</a>
 

 

