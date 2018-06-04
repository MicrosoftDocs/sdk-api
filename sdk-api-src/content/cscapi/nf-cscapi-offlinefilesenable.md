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

# OfflineFilesEnable function


## -description


Enables or disables the Offline Files feature.


## -parameters




### -param bEnable [in]

Specify <b>TRUE</b> to enable Offline Files, or <b>FALSE</b> to disable.


### -param pbRebootRequired [out]

Receives <b>TRUE</b> if a system restart is necessary to apply the desired configuration, or <b>FALSE</b> otherwise.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error value otherwise.




## -remarks



The Offline Files feature is implemented in two parts, the Offline Files service and the CSC driver.  When the  Offline Files feature is enabled, this means that the CSC driver's start type is set to SERVICE_SYSTEM_START and the Offline Files service's start type is set to SERVICE_AUTO_START.  If the driver is not already running, the caller must restart the computer after calling this method.

Disabling Offline Files disables both the service and the driver.  To disable the feature, the caller must restart the computer after calling this method.

The caller must be an administrator on the local computer.



