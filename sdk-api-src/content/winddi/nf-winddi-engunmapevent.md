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

# EngUnmapEvent function


## -description


The <b>EngUnmapEvent</b> function cleans up the kernel-mode resources allocated for a mapped user-mode event.


## -parameters




### -param pEvent [in]

Pointer to an event object returned from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.


## -returns



<b>EngUnmapEvent</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



The display driver should call <b>EngUnmapEvent</b> when it is notified that the process (typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff564207">EngCreateDriverObj</a>) that created the user-mode event has terminated. The display driver can also call <b>EngUnmapEvent</b> to perform its own cleanup. The display and miniport drivers should not touch the event object after <b>EngUnmapEvent</b> has been called.

The display driver can call <b>EngUnmapEvent</b> only for an event object returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>. It must not call this function for an event object returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564207">EngCreateDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

