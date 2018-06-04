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

# CM_Disable_DevNode function


## -description


The <b>CM_Disable_DevNode</b> function disables a device.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param ulFlags [in]

Disable flags:





#### CM_DISABLE_UI_NOT_OK

Do not display any interface to the user if the attempt to disable the device fails.



#### CM_DISABLE_PERSIST

Disables the device across reboots.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



By default, <b>CM_Disable_DevNode</b> disables a device at one time, but after reboot the device is enabled again. Starting in Windows 10, you can specify the <b>CM_DISABLE_PERSIST</b> flag to disable the device across reboots.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538015">CM_Enable_DevNode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

