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

# LPM_Deinitialize function


## -description


The 
<i>LPM_Deinitialize</i> function allows the PCM to instruct LPMs to deinitialize, whether due to system shutdown or a change in Designated Subnet Bandwidth Manager (DSBM) status. This occurs when the Admission Control Service no longer needs to do policy based–admission control, such as when a demotion from DSBM status occurs. LPMs should free resources, close connections to external entities such as policy server or directory services, and perform any other cleanup necessary to properly relinquish LPM activities. The PCM will unload the DLL after 
<i>LPM_Deinitialize</i> returns.


## -parameters




### -param LpmHandle

Unique handle to the LPM, as supplied through 
<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a> during initialization.


## -returns



If another value is returned from 
<i>LPM_Deinitialize</i>, the PCM will record the name of this DLL (implementations of LPMs are always in the form of a DLL), as well as this return value, in the Event Log.




## -remarks



LPMs do not need to return errors for outstanding requests when 
<i>LPM_Deinitialize</i> is called; PCM assumes LPV_REJECT for outstanding requests. LPMs should deinitialize synchronously before returning. If an LPM has been loaded and initialized multiple times to facilitate the handling of multiple PE types, the PCM will call 
<i>LPM_Deinitialize</i> multiple times as well.




## -see-also




<a href="https://msdn.microsoft.com/00f4ab59-8808-4bcb-8258-5aad113ad2b5">LPM_Initialize</a>
 

 

