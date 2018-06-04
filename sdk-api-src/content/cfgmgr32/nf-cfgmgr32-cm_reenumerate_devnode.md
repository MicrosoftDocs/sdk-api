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

# CM_Reenumerate_DevNode function


## -description


The <b>CM_Reenumerate_DevNode</b> function enumerates the devices identified by a specified device node and all of its children.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Caller-supplied flags that specify how reenumeration should occur. This parameter can be set to a combination of the following flags, as noted:





#### CM_REENUMERATE_ASYNCHRONOUS

Reenumeration should occur asynchronously. The call to this function returns immediately after the PnP manager receives the reenumeration request. If this flag is set, the CM_REENUMERATE_SYNCHRONOUS flag should not also be set.



#### CM_REENUMERATE_NORMAL

Specifies default reenumeration behavior, in which reenumeration occurs synchronously. This flag is functionally equivalent to CM_REENUMERATE_SYNCHRONOUS.



#### CM_REENUMERATE_RETRY_INSTALLATION

Specifies that Plug and Play should make another attempt to install any devices in the specified subtree that have been detected but are not yet configured, or are marked as needing reinstallation, or for which installation must be completed. This flag can be set along with <i>either</i> the CM_REENUMERATE_SYNCHRONOUS flag <i>or</i> the CM_REENUMERATE_ASYNCHRONOUS flag.

This flag must be used with extreme caution, because it can cause the PnP manager to prompt the user to perform installation of any such devices. Currently, only components such as Device Manager and Hardware Wizard use this flag, to allow the user to retry installation of devices that might already have been detected but are not currently installed.



#### CM_REENUMERATE_SYNCHRONOUS

Reenumeration should occur synchronously. The call to this function returns when all devices in the specified subtree have been reenumerated. If this flag is set, the CM_REENUMERATE_ASYNCHRONOUS flag should not also be set. This flag is functionally equivalent to CM_REENUMERATE_NORMAL.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



If the specified device node represents a hardware or software bus device, the PnP manager queries the device's drivers for a list of children, then attempts to configure and start any child devices that were not previously configured. The PnP manager also initiates surprise-removal of devices that are no longer present (see <a href="https://msdn.microsoft.com/library/windows/hardware/ff551760">IRP_MN_SURPRISE_REMOVAL</a>).

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539766">CM_Reenumerate_DevNode_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551760">IRP_MN_SURPRISE_REMOVAL</a>
 

 

