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

# _PDH_DATA_ITEM_PATH_ELEMENTS_A structure


## -description



			The 
<b>PDH_DATA_ITEM_PATH_ELEMENTS</b> structure contains the path elements of a specific data item.
		


## -struct-fields




### -field szMachineName

Pointer to a null-terminated string that specifies the name of the computer where the data item resides.


### -field ObjectGUID

GUID of the object where the data item resides.


### -field dwItemId

Identifier of the data item.


### -field szInstanceName

Pointer to a null-terminated string that specifies the name of the data item instance.


## -see-also




<a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a>
 

 

