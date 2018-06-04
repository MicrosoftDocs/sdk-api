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

# _RM_UNIQUE_PROCESS structure


## -description


Uniquely identifies a process by its PID and the time the process began.  An array of <b>RM_UNIQUE_PROCESS</b> structures can be passed to  the <a href="https://msdn.microsoft.com/9ac94461-bf75-4517-b47e-23d82474efe8">RmRegisterResources</a> function. 


## -struct-fields




### -field dwProcessId

The product identifier (PID).


### -field ProcessStartTime

The creation time of the process. The time is provided as a <b>FILETIME</b> structure that is returned by the <i>lpCreationTime</i> parameter of the <a href="https://msdn.microsoft.com/4c1e8bd4-5ed2-4c97-bc4f-1083a8b24623">GetProcessTimes</a> function. 


## -remarks



The <b>RM_UNIQUE_PROCESS</b> structure can be used to uniquely identify an application in an <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structure or  registered with the Restart Manager session by the <a href="https://msdn.microsoft.com/9ac94461-bf75-4517-b47e-23d82474efe8">RmRegisterResources</a> function.



