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

# EngCreateEvent function


## -description


The <b>EngCreateEvent</b> function creates a synchronization event object that can be used to synchronize hardware access between a display driver and the video miniport driver.


## -parameters




### -param ppEvent [out]

Pointer to a location in which a valid event object is returned.


## -returns



<b>EngCreateEvent</b> returns <b>TRUE</b> if it is successful in creating an event object. Otherwise, it returns <b>FALSE</b>.




## -remarks



<b>EngCreateEvent</b> creates a synchronization event object, which is initialized to the nonsignaled state.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564801">EngDeleteEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565013">EngSetEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565461">EngWaitForSingleObject</a>
 

 

