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

# WakeByAddressAll function


## -description


Wakes all threads that are waiting for the value of an address to change.


## -parameters




### -param Address [in]

The address to signal. If any threads have previously called 
      <a href="https://msdn.microsoft.com/d40de436-f71e-47f6-a8c3-549c2699eb4c">WaitOnAddress</a> for this address, the system wakes all 
      of the waiting threads.


## -returns



This function does not return a value.




## -remarks



Windows Store apps developers may need to obtain synchronization.lib by installing the <a href="http://go.microsoft.com/fwlink/p/?LinkID=258383">Windows Software Development Kit (SDK) for Windows 8</a>.

Only threads within the same process can be woken.




## -see-also




<a href="https://msdn.microsoft.com/d40de436-f71e-47f6-a8c3-549c2699eb4c">WaitOnAddress</a>
 

 

