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

# CM_Setup_DevNode function


## -description


The <b>CM_Setup_DevNode</b> function restarts a device instance that is not running because there is a problem with the device configuration.


## -parameters




### -param dnDevInst [in]

A device instance handle that is bound to the local system.


### -param ulFlags [in]

One of the following flag values:





#### CM_SETUP_DEVNODE_READY

Restarts a device instance that is not running because of a problem with the device configuration.



#### CM_SETUP_DEVNODE_RESET (Windows XP and later versions of Windows)

Resets a device instance that has the no restart device status flag set. The no restart device status flag is set if a device is removed by calling <b>CM_Query_And_Remove_SubTree</b> or <b>CM_Query_And_Remove_SubTree_Ex</b> and specifying the CM_REMOVE_NO_RESTART flag.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise it returns one of the error codes with "CR_" prefix that are defined in <i>Cfgmgr32.h</i>.




## -remarks



<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">Device installation applications</a> should use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a> request to restart a device instead of using this function. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device. 

If a device instance does not have a problem and is already started, <b>CM_Setup_DevNode</b> returns without changing the status of the device instance.

Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538517">CM_Get_DevNode_Status_Ex</a> to determine the status and problem code for a device instance. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538517">CM_Get_DevNode_Status_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539722">CM_Query_And_Remove_SubTree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539727">CM_Query_And_Remove_SubTree_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a>
 

 

