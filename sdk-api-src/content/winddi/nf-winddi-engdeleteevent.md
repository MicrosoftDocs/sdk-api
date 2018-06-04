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

# EngDeleteEvent function


## -description


The <b>EngDeleteEvent</b> function deletes the specified event object.


## -parameters




### -param pEvent [in]

Pointer to the event object to be deleted.


## -returns



<b>EngDeleteEvent</b> returns <b>TRUE</b> if it is successful in deleting the specified event object. It returns <b>FALSE</b> if the caller attempts to delete a mapped user event.




## -remarks



A display driver can call <b>EngDeleteEvent</b> only with an event object returned from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a> function, and must not call it to delete event objects returned from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.

Before calling <b>EngDeleteEvent</b>, the display driver must notify all holders of the specified event object that it is about to become invalid.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

