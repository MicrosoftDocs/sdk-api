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

# OfflineFilesQueryStatusEx function


## -description


Determines whether the Offline Files feature is enabled and, if so, whether it is active and available. This function is identical to the <a href="https://msdn.microsoft.com/2b3a77cd-e874-42fb-8bfa-6d6b26866153">OfflineFilesQueryStatus</a> function, except that it has an additional output parameter.


## -parameters




### -param pbActive [out]

Receives <b>TRUE</b> if both the CSC driver and Offline Files Service are in the running state, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.


### -param pbEnabled [out]

Receives <b>TRUE</b> if the CSC driver's start type is set to <b>SERVICE_SYSTEM_START</b> and the Offline Files service's start type is set to <b>SERVICE_AUTO_START</b>, or <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.


### -param pbAvailable [out]

Receives <b>TRUE</b> if the Offline Files Service is ready to be started without requiring the computer to be restarted, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.




## -remarks



If the <i>pbAvailable</i> parameter is <b>TRUE</b> on return, the caller can use the <a href="https://msdn.microsoft.com/79060780-A2C1-45CE-BB9A-75DF433C3F3C">OfflineFilesStart</a> function to start the Offline Files feature.




## -see-also




<a href="https://msdn.microsoft.com/2b3a77cd-e874-42fb-8bfa-6d6b26866153">OfflineFilesQueryStatus</a>
 

 

