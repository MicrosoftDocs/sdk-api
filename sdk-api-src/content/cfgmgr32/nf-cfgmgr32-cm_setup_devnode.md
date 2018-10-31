---
UID: NF:cfgmgr32.CM_Setup_DevNode
title: CM_Setup_DevNode function
author: windows-sdk-content
description: The CM_Setup_DevNode function restarts a device instance that is not running because there is a problem with the device configuration.
old-location: devinst\cm_setup_devnode.htm
tech.root: devinst
ms.assetid: 94d0023d-d93f-42da-b2fc-54b9d8831b9b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CM_Setup_DevNode, CM_Setup_DevNode function [Device and Driver Installation], cfgmgr32/CM_Setup_DevNode, cfgmgrfn_e8515529-d4bc-4411-a5cf-18bc4f4d7500.xml, devinst.cm_setup_devnode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Setup_DevNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">Device installation applications</a> should use the <a href="https://msdn.microsoft.com/62f3380d-8cd1-4f4c-a727-1285de081b9e">DIF_PROPERTYCHANGE</a> request to restart a device instead of using this function. The DIF_PROPERTYCHANGE request can be used to enable, disable, restart, stop, or change the properties of a device. 

If a device instance does not have a problem and is already started, <b>CM_Setup_DevNode</b> returns without changing the status of the device instance.

Call <a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a> or <a href="https://msdn.microsoft.com/3e7dd781-7f99-4c49-bbe1-8d2e63cff553">CM_Get_DevNode_Status_Ex</a> to determine the status and problem code for a device instance. 




## -see-also




<a href="https://msdn.microsoft.com/7347c142-8bcf-43b3-aef0-5f99e2873560">CM_Get_DevNode_Status</a>



<a href="https://msdn.microsoft.com/3e7dd781-7f99-4c49-bbe1-8d2e63cff553">CM_Get_DevNode_Status_Ex</a>



<a href="https://msdn.microsoft.com/0a80cddd-d5be-42cb-ba11-0a3292b973a3">CM_Query_And_Remove_SubTree</a>



<a href="https://msdn.microsoft.com/c8a3af37-0886-4187-9cdb-49616bcb04a9">CM_Query_And_Remove_SubTree_Ex</a>



<a href="https://msdn.microsoft.com/62f3380d-8cd1-4f4c-a727-1285de081b9e">DIF_PROPERTYCHANGE</a>
 

 

