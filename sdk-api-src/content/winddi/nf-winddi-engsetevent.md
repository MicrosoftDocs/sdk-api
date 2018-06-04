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

# EngSetEvent function


## -description


The <b>EngSetEvent</b> function sets the specified event object to the signaled state, and returns the event object's previous state.


## -parameters




### -param pEvent [in]

Pointer to the event object that is to be set to the signaled state. This event object was returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.


## -returns



<b>EngSetEvent</b> returns a nonzero value if the event object's previous state was signaled.




## -remarks



Every event object is in either the signaled state or the nonsignaled state. Calling <b>EngSetEvent</b> causes the event object to be set to the signaled state.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565461">EngWaitForSingleObject</a>
 

 

