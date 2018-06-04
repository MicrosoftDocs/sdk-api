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

# CM_Locate_DevNodeW function


## -description


The <b>CM_Locate_DevNode</b> function obtains a device instance handle to the device node that is associated with a specified <a href="devinst.device_instance_ids">device instance ID</a> on the local machine.


## -parameters




### -param pdnDevInst [out]

A pointer to a device instance handle that <b>CM_Locate_DevNode</b> retrieves. The retrieved handle is bound to the local machine.


### -param pDeviceID [in, optional]

A pointer to a NULL-terminated string representing a <a href="devinst.device_instance_ids">device instance ID</a>. If this value is <b>NULL</b>, or if it points to a zero-length string, the function retrieves a device instance handle to the device at the root of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543194">device tree</a>.


### -param ulFlags [in]

A variable of ULONG type that supplies one of the following flag values that apply if the caller supplies a device instance identifier:





#### CM_LOCATE_DEVNODE_NORMAL

The function retrieves the device instance handle for the specified device only if the device is currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_PHANTOM

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or the device is a <a href="https://msdn.microsoft.com/50c44afb-5b6b-44cb-90dd-d7ae83b2d991">nonpresent device</a> that is not currently configured in the device tree. 



#### CM_LOCATE_DEVNODE_CANCELREMOVE

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or in the process of being removed from the device tree. If the device is in the process of being removed, the function cancels the removal of the device.



#### CM_LOCATE_DEVNODE_NOVALIDATION

Not used.


##### - ulFlags.CM_LOCATE_DEVNODE_CANCELREMOVE

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or in the process of being removed from the device tree. If the device is in the process of being removed, the function cancels the removal of the device.


##### - ulFlags.CM_LOCATE_DEVNODE_NORMAL

The function retrieves the device instance handle for the specified device only if the device is currently configured in the device tree. 


##### - ulFlags.CM_LOCATE_DEVNODE_NOVALIDATION

Not used.


##### - ulFlags.CM_LOCATE_DEVNODE_PHANTOM

The function retrieves a device instance handle for the specified device if the device is currently configured in the device tree or the device is a <a href="https://msdn.microsoft.com/50c44afb-5b6b-44cb-90dd-d7ae83b2d991">nonpresent device</a> that is not currently configured in the device tree. 


## -returns



If the operation succeeds, <b>CM_Locate_DevNode</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_<i>Xxx</i> error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538751">CM_Locate_DevNode_Ex</a>
 

 

