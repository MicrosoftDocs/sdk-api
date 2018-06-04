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

# IOfflineFilesEventsFilter::GetPathFilter


## -description


Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.


## -parameters




### -param ppszFilter [out]

Receives a fully qualified UNC path string identifying the path associated with the filter. The memory for this string must be allocated using the <a href="_com_cotaskmemalloc">CoTaskMemAlloc</a> function.


### -param pMatch [out]

Receives an <a href="https://msdn.microsoft.com/fae3d36d-b5f3-45ae-97f2-41fd6045d976">OFFLINEFILES_PATHFILTER_MATCH</a> enumeration  value indicating which descendants of the filter path are to be included in the set of events delivered to the event sink.


## -returns



Return <b>S_OK</b> if implemented, <b>E_NOTIMPL</b> if not implemented.




## -see-also




<a href="https://msdn.microsoft.com/8c2c793e-c91c-4ca7-a03c-e349de00de6c">IOfflineFilesEventsFilter</a>
 

 

