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

# CM_Open_DevNode_Key function


## -description


The <b>CM_Open_DevNode_Key</b> function opens a registry key for device-specific configuration information.


## -parameters




### -param dnDevNode [in]

Caller-supplied device instance handle that is bound to the local machine


### -param samDesired [in]

The registry security access that is required for the requested key. 


### -param ulHardwareProfile [in]

The hardware profile to open if <i>ulFlags</i> includes CM_REGISTRY_CONFIG. If this value is zero, the key for the current hardware profile is opened.


### -param Disposition [in]

Specifies how the registry key is to be opened. May be one of the following values:





#### RegDisposition_OpenAlways

Open the key if it exists. Otherwise, create the key.



#### RegDisposition_OpenExisting

Open the key only if it exists.


### -param phkDevice [out]

Pointer to an HKEY that will receive the opened key upon success.


### -param ulFlags [in]

Open device node key flags. Indicates the scope and type of registry storage key to open.  Can be a combination of the following flags:





#### CM_REGISTRY_HARDWARE

Open the device’s hardware key. Do not combine with CM_REGISTRY_SOFTWARE.



#### CM_REGISTRY_SOFTWARE

Open the device’s software key. Do not combine with CM_REGISTRY_HARDWARE.



#### CM_REGISTRY_USER

Open the per-user key for the current user. Do not combine with CM_REGISTRY_CONFIG.



#### CM_REGISTRY_CONFIG

Open the key that stores hardware profile-specific configuration information. Do not combine with CM_REGISTRY_USER.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Close the handle returned from this function by calling <b>RegCloseKey</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537973">CM_Delete_DevNode_Key</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552079">SetupDiOpenDevRegKey</a>
 

 

