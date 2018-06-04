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

# IsSystemResumeAutomatic function


## -description


Determines the current state of the computer.


## -parameters






## -returns



If the system was restored to the working state automatically and the user is not active, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



The 
<a href="https://msdn.microsoft.com/cd331f79-b64d-479e-aea8-5118ccc87224">PBT_APMRESUMEAUTOMATIC</a> event is broadcast when the system wakes automatically to handle an event. The user is generally not present. If the system detects any user activity after broadcasting the 
PBT_APMRESUMEAUTOMATIC event, it will broadcast the 
<a href="https://msdn.microsoft.com/9058a2ff-9b8e-48e5-accb-4810c8598294">PBT_APMRESUMESUSPEND</a> event to let applications know they can resume full interaction with the user.




## -see-also




<a href="https://msdn.microsoft.com/cd331f79-b64d-479e-aea8-5118ccc87224">PBT_APMRESUMEAUTOMATIC</a>



<a href="https://msdn.microsoft.com/9058a2ff-9b8e-48e5-accb-4810c8598294">PBT_APMRESUMESUSPEND</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

