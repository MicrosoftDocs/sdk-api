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

# OfflineFilesQueryStatus function


## -description


Determines whether the Offline Files feature is enabled and, if so, whether it is active.


## -parameters




### -param pbActive [out]

Receives <b>TRUE</b> if both the CSC driver and Offline Files Service are in the running state, or  <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.


### -param pbEnabled [out]

Receives <b>TRUE</b> if the CSC driver's start type is set to <b>SERVICE_SYSTEM_START</b> and the Offline Files service's start type is set to <b>SERVICE_AUTO_START</b>, or <b>FALSE</b> otherwise. This parameter is optional and can be <b>NULL</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.




## -remarks



If the values returned in the <i>pbActive</i> and <i>pbEnabled</i> parameters are not both <b>TRUE</b>, the caller must restart the computer to enable or disable the Offline Files feature.  If one of the values is still <b>FALSE</b> after the computer is restarted, check the system event logs to identify the problem with starting either the CSC driver or the Offline Files service.




## -see-also




<a href="https://msdn.microsoft.com/1916F3F7-3B99-40CA-B503-EA1D10991BF4">OfflineFilesQueryStatusEx</a>
 

 

