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

# CM_Delete_DevNode_Key function


## -description


The <b>CM_Delete_DevNode_Key</b> function deletes the specified user-accessible registry keys that are associated with a device.


## -parameters




### -param dnDevNode [in]

Device instance handle that is bound to the local machine.


### -param ulHardwareProfile [in]

The hardware profile to delete if <i>ulFlags</i> includes CM_REGISTRY_CONFIG. If this value is zero, the key for the current hardware profile is deleted. If this value is 0xFFFFFFFF, the registry keys for all hardware profiles are deleted.


### -param ulFlags [in]

Delete device node key flags. Indicates the scope and type of registry storage key to delete.  Can be a combination of the following flags:





#### CM_REGISTRY_HARDWARE

Delete the device’s hardware key. Do not combine with CM_REGISTRY_SOFTWARE.



#### CM_REGISTRY_SOFTWARE

Delete the device’s software key. Do not combine with CM_REGISTRY_HARDWARE.



#### CM_REGISTRY_USER

Delete the per-user key for the current user. Do not combine with CM_REGISTRY_CONFIG.



#### CM_REGISTRY_CONFIG

Delete the key that stores hardware profile-specific configuration information. Do not combine with CM_REGISTRY_USER.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538823">CM_Open_DevNode_Key</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550991">SetupDiDeleteDevRegKey</a>
 

 

