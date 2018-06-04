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

# _PDH_COUNTER_PATH_ELEMENTS_W structure


## -description



			The 
<b>PDH_COUNTER_PATH_ELEMENTS</b> structure contains the components of a counter path. 


## -struct-fields




### -field szMachineName

Pointer to a null-terminated string that specifies the computer name. 


### -field szObjectName

Pointer to a null-terminated string that specifies the object name.


### -field szInstanceName

Pointer to a null-terminated string that specifies the instance name. Can contain a wildcard character.


### -field szParentInstance

Pointer to a null-terminated string that specifies the parent instance name. Can contain a wildcard character.


### -field dwInstanceIndex

Index used to uniquely identify duplicate instance names.


### -field szCounterName

Pointer to a null-terminated string that specifies the counter name.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a> to create a counter path and by <a href="https://msdn.microsoft.com/760b94e9-88df-4f7d-92e9-333d682779f6">PdhParseCounterPath</a> to parse a counter path.

When you allocate memory for this structure, allocate enough memory for the member strings, such as <b>szCounterName</b>, that are appended to the end of this structure.




## -see-also




<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>



<a href="https://msdn.microsoft.com/760b94e9-88df-4f7d-92e9-333d682779f6">PdhParseCounterPath</a>
 

 

