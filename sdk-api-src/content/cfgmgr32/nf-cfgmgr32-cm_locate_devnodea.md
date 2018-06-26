---
UID: NF:cfgmgr32.CM_Locate_DevNodeA
title: CM_Locate_DevNodeA function
author: windows-sdk-content
description: The CM_Locate_DevNode function obtains a device instance handle to the device node that is associated with a specified device instance ID on the local machine.
old-location: devinst\cm_locate_devnode.htm
old-project: devinst
ms.assetid: b0bb2510-44be-4598-96ea-9b8fdcc7f7c6
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CM_Locate_DevNode, CM_Locate_DevNode function [Device and Driver Installation], CM_Locate_DevNodeA, CM_Locate_DevNodeW, cfgmgr32/CM_Locate_DevNode, cfgmgr32/CM_Locate_DevNodeA, cfgmgr32/CM_Locate_DevNodeW, cfgmgrfn_70e99ef3-9630-4088-8fcb-f6c7123f2cb5.xml, devinst.cm_locate_devnode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Locate_DevNodeW (Unicode) and CM_Locate_DevNodeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-Devices-Config-L1-1-0.dll
 - API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
 - CM_Locate_DevNode
 - CM_Locate_DevNodeA
 - CM_Locate_DevNodeW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Locate_DevNodeA function


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


## -returns



If the operation succeeds, <b>CM_Locate_DevNode</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_<i>Xxx</i> error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538751">CM_Locate_DevNode_Ex</a>
 

 

