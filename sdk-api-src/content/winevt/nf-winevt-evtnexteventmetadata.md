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

# EvtNextEventMetadata function


## -description


Gets an event definition from the enumerator.


## -parameters




### -param EventMetadataEnum [in]

A handle to the event definition enumerator that the <a href="https://msdn.microsoft.com/e1d2e5d5-89db-4bda-9803-37f26d1fe30f">EvtOpenEventMetadataEnum</a> function returns.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the event's metadata; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



Call this function in a loop until the function returns <b>NULL</b> and the error code is ERROR_NO_MORE_ITEMS.

To get a property from the event definition, call the <a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a> function.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the event definition handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a>
 

 

